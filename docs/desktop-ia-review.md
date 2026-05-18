# T005 Desktop IA and Navigation Review

Machine: worker-desktop
Task: T005
Status: todo
Source reviewed: http://192.168.31.113:5173/#tasks

## Scope

Reviewed the desktop information architecture and navigation exposed by the current Zhidou app prototype. The review is based on the running Vite page, its public `App.tsx` source, and its `App.css` layout rules.

## Current Structure

The page is a single-page prototype with anchored sections:

- Header navigation: Knowledge Feed, Topic Paths, Creator Workflow, Worker Board.
- Hero: product positioning and primary calls to action.
- Metrics: content unit, core users, first-stage scope.
- Knowledge Feed: featured note cards.
- Topic Paths: grouped learning paths.
- Creator Workflow: publishing workflow.
- MVP Scope: next development order.
- Worker Board: task cards for distributed machines.

## Findings

1. The primary navigation is clear but incomplete for the visible page model.
   The top navigation links to `#feed`, `#paths`, `#creator`, and `#tasks`, but there is no direct navigation item for `#concept` / MVP Scope. The hero secondary CTA links there, so the section is part of the desktop journey but not represented in the main nav.

2. The page mixes product-facing IA with internal worker coordination.
   The Worker Board is useful for project coordination, but it currently lives in the same top-level navigation as user-facing product areas. On desktop, this makes the prototype read partly like a product landing page and partly like an internal task dashboard. If the board remains visible, it should be visually and structurally labeled as internal.

3. The desktop content order is logical for a prototype.
   The sequence moves from positioning, to content examples, to topic organization, to creator workflow, then to implementation scope. This supports a first-pass product narrative for stakeholders.

4. The hero CTA path is partially redundant.
   The primary CTA links to Knowledge Feed, which is also the first nav item. The secondary CTA links to MVP Scope, which is not in nav. This is workable, but the CTA pair currently mixes user preview and planning detail. A cleaner desktop IA would pair `View prototype` with `Review MVP scope` and include both destinations in the navigation or keep MVP Scope out of the main user journey.

5. Section naming is inconsistent across Chinese and English labels.
   Eyebrows use English labels such as `Knowledge Feed`, `Topic Paths`, `Creator Workflow`, `MVP Scope`, and `Worker Board`, while visible navigation labels are Chinese. This is acceptable for an internal prototype, but a public-facing desktop IA should standardize whether section labels are product-facing Chinese or internal bilingual labels.

6. The task board card layout scales well on desktop.
   Four cards in a single row make ownership and output paths easy to scan at desktop width. The `overflow-wrap: anywhere` rule protects long output paths. The board is fit for internal use.

## Recommendations

1. Add MVP Scope to the desktop navigation, or remove the hero secondary CTA to `#concept`.
   This will make the available destinations match the page model.

2. Separate internal coordination from product navigation.
   Preferred option: keep Worker Board on the page for development builds, but label it as internal and place it after a divider or under an `Internal` grouping. If the page is meant for users, hide it from primary nav.

3. Normalize section labels.
   Use Chinese section names for user-facing IA and reserve English labels for small internal metadata only.

4. Tighten CTA language.
   Recommended desktop CTA pair:
   - Primary: `View knowledge feed`
   - Secondary: `View MVP scope`

5. Define the desktop IA target state before adding more pages.
   Suggested top-level IA:
   - Knowledge feed
   - Topic paths
   - Creator workflow
   - MVP scope
   - Internal worker board

## Suggested Next Work

- Update `TASKS.md` or the task board source to mark T005 as `doing` before implementation changes.
- If implementation is approved, adjust header navigation to include MVP Scope and move Worker Board under a clearer internal label.
- Re-check the desktop viewport after changes at 1280px and 1440px widths.

## Result

T005 review is complete. No application files were changed.
