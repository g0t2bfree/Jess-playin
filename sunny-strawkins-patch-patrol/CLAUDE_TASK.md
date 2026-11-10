# Claude Code: Build and Finish Sunny Strawkins: Patch Patrol

You have a real, existing HTML5 prototype in this folder: `index.html`. **Read and run it before deciding what to change.** I need you to take over actual implementation, testing, debugging, polish, and release packaging with minimal back-and-forth. Do not respond with a plan and then stop; start executing.

## User goals
- Release a polished, delightful **mobile-first HTML5 browser game** on itch.io, enjoyable on desktop too.
- Fast start, no account, no external services, no phone-specific developer tools needed by the player.
- Keep the game small enough to ship; it is a standalone spin-off and teaser for a much deeper planned PC scarecrow-defense game. Do not quietly reduce or replace the larger PC vision.
- Do not publish publicly without explicit user authorization.

## Canon / fantasy
Sunny Strawkins is an irresistibly adorable **kawaii toddler-sized** scarecrow in a warm storybook farm. Later merge forms can grow visibly stronger/taller, with a sweet 'big brother' feel; do not make base Sunny adult-sized or horror-themed. Pip is the helpful farm dog. A farmer protects the sunflowers, garden, and ultimately livestock from invading pests/birds. Soft cohesive pastel/harvest palette, friendly animation, expressive feedback. Avoid generic circles where finished art is expected, mismatched clipped sprites, or copyright-restricted art.

## Required launch version: complete playable loop
1. Start screen and 10–20 second interactive tutorial. Player understands goal, plant cost, merge selection and Pip's cooldown.
2. Four distinct rows/lanes; responsive garden board, clear occupied and free tiles, controls large enough for mobile.
3. Player plants adorable Level-1 scarecrows using straw. Tap a Level-N then another Level-N to merge; drag merging is an optional second control. Max level at least four; distinct silhouettes, strength/attack upgrades.
4. Incoming birds (crows and at least two later variants) approach in waves; defensive scarecrows automatically target birds in their lanes; shots/hits/misses/deaths are visible and logically correct.
5. Five increasingly challenging waves, between-wave rewards/breathers, straw regeneration and rewards, ability to lose farm hearts; deterministic victory and game-over outcomes with restart.
6. Pip's special bark has a visible cooldown and meaningful tactical effect.
7. Scoring/high-score persistence through localStorage with guarded fallback; pause/resume controls; no stuck modal or impossible state.
8. Clear audio toggle, safe sound behavior after mobile user gesture, attractive menus, end screens, settings.
9. Fun visual and audio feedback, coherent mobile-first polish; artwork must be original or commercially licensable.

## Engineering
- Use the existing `index.html` as baseline; refactor if it materially helps. Keep production build simple, static, offline-capable where feasible, with correct relative paths.
- Prefer no runtime dependencies and avoid a giant framework unless essential.
- Add reproducible automated tests (e.g. Playwright with a local static server) for start, plant, straw cost, valid/invalid merge, waves, enemy damage, Pip, pause, victory, loss, restart, mobile touches, portrait/narrow viewport, high-score persistence, no console errors.
- Accelerated time or test hooks are allowed in **test builds**, but no cheating in release builds.
- Execute the tests and preserve accurate results. Do not call untested behavior 'passed'.
- Check actual browser rendering at common portrait phone dimensions and desktop sizes. Fix clipping, input offsets, portrait scrolling conflicts, pointer capture, performance, and visual glitches.
- Check keyboard/mouse + Android touch, no audio autoplay errors, no network/CDN dependence, no external tracking.
- Use small clean commits and do not edit unrelated folders in this repository.

## Concrete release deliverables
- Updated, fully functioning HTML5 source code in this project folder
- Game README with clear controls
- Playwright automated tests and a command to execute them, plus actual summary of their results
- Final verified `Sunny_Strawkins_Patch_Patrol_HTML5.zip` with `index.html` at the ZIP root
- Cover image at least 630×500, and 3–5 truthful in-game screenshots for itch.io
- Polished itch.io description and release notes/changelog
- A small release checklist with remaining real-world testing (if any) and any unverified items marked clearly

## Platform / deployment
Existing itch.io draft account: `g0t2bfree`. Existing editor page is authenticated and may not be available to you: `https://itch.io/game/edit/5334789`. **Do not get stuck on that link.** Build and verify locally from this GitHub source. If connected itch.io credentials or Butler are available, prepare a secure workflow, but do not expose tokens in source or change public visibility without approval.

## Work style
I am on a phone, have limited time, and cannot babysit your work. Do not ask routine choices. Make reasonable decisions and **execute**. If tool/site access is blocked, continue with all independent work instead of asking me to forward files or recreate the brief. Only request user intervention for a true permission/authentication/irreversible publishing decision. Finish with working artifacts, exact test commands and test outcomes, and a compact list of any genuine blockers.