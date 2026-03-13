# Ecosystem: linkedin-ads-campaign-playbook

How this repo connects to the rest of the Forma Norden GTM library.

## Works With

| Repo | Relationship | When to use together |
|------|-------------|---------------------|
| ``linkedin-claude-code-workflow`` | Parallel | The workflow executes what the playbook strategizes; they work in tandem. |
| ``cold-email-copy-playbook`` | Downstream | Ad engagement provides warm intent for outbound email sequences. |
| ``signal-based-list-building-workflow`` | Upstream | Target lists defined here are uploaded as Matched Audiences. |
| ``linkedin-profile-dm-conversion-playbook`` | Parallel | Organic / DM motions complement paid ad awareness simultaneously. |

## Suggested Skill Chains

1. Program Launch: ``list-icp-definition`` > ``linkedin-ads-funnel-architect`` > ``linkedin-ads-audience-targeting`` > ``linkedin-ads-copy-framework``
2. BDR Handoff: ``linkedin-ads-measurement-attribution`` > ``linkedin-ads-outbound-sync`` > ``copy-btl-practitioner-messaging``
