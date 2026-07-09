MISSION
Build GitHub Studio UI and Mission Artifact Publisher

CONTEXT
No additional context supplied.

COMPLETION CRITERIA
Build a GitHub Studio UI and Mission Artifact Publisher inside IronIC.

Current working terminal flow:
- Mission artifacts persist under /data/missions/<mission-id>/artifacts/
- mission_stage_artifact.sh can stage a mission artifact into public_exports or github_staging
- github_stage_repo.sh stages files into the local GitHub clone
- github_secret_scan.sh scans for secrets
- github_approve_push.sh records human approval
- github_push_approved.sh pushes approved commits
- Latest successful public test pushed commit de11c926cc2486f50061cfec62688dd913728f06 to labs

Goal:
Make this usable from inside IronIC.

Required UI:
1. Add a GitHub Studio page.
2. Show all configured repos:
   - platform-core
   - studio
   - labs
   - ai-automation
   - rwa-framework
3. Show repo visibility, mode, staging path, local clone, allowed paths, blocked paths.
4. Show latest staging receipts and push receipts.
5. Add a Mission Artifact Publisher section:
   - select mission
   - select artifact
   - select target repo
   - enter destination path
   - stage artifact
   - run secret scan
   - request push approval
   - push approved commit
6. Public repos must display a PUBLIC WARNING.
7. Private repos must display a PRIVATE badge.
8. No push may happen without human approval.
9. No public staging may happen if secret scan fails.
10. Every stage and push must create a receipt.

Success criteria:
- I can select a mission artifact in IronIC and stage it to labs.
- I can see the staged file and receipt.
- I can approve and push from the GitHub Studio UI.
- The UI shows the final commit hash.
- The terminal flow still works as fallback.

CAPABILITIES
- None attached

CONTROL NOTE
No external submission, signature, KYC, payment, wallet action, or irreversible change was performed.