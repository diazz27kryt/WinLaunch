# WinLaunch Beta 0.1

WinLaunch is an Android Minecraft: Java Edition launcher project based on MojoLauncher.

## Product direction

- Brand: WinLaunch
- Release channel: Beta Test
- UI direction: horizontal-first launcher interface
- Visual style: dark / white Liquid Glass, translucent surfaces, subtle borders and rounded panels
- Account direction: local offline profiles as the default account flow
- Core engine: retain the upstream Minecraft runtime, version installation and mod-loader support

## Main screen layout

1. Top bar: WinLaunch wordmark on the left; account, downloads and settings actions on the right.
2. Navigation: Главная, Сборки, Моды, Ресурсы, Аккаунты, Настройки.
3. Main content: selected Minecraft profile and version card on the left; large world artwork on the right.
4. Primary action: Играть.
5. Footer: memory allocation, Android edition and WinLaunch version.

## Implementation principles

- Keep upstream game launching and installation logic intact while the UI is being redesigned.
- Prefer landscape-specific resources in `res/layout-land`; retain a usable portrait fallback until the user explicitly decides otherwise.
- Do not remove Microsoft authentication code until offline-profile behavior and server compatibility have been reviewed.
- Preserve upstream and third-party license notices. MojoLauncher is licensed under LGPL-3.0; see `LICENSE`.
- Treat each beta step as a buildable, reviewable change.

## Beta 0.1 milestones

- [x] Create a separate WinLaunch fork and working branch.
- [x] Set the displayed app name to WinLaunch (default and Russian resources).
- [ ] Implement the horizontal Liquid Glass main screen.
- [ ] Rebrand application ID, launcher icon and version metadata safely.
- [ ] Verify Android CI and publish a debug APK artifact.
