ZMK one-key Bluetooth test package

Goal:
- nice!nano-compatible board
- switch between Pro Micro pin D9 and GND
- pressing the switch sends the A key over Bluetooth

Contents:
- build.yaml: replaces the current build.yaml
- config/test_one.keymap: one-key keymap
- boards/shields/test_one/: custom shield definition

How to use:
1. Back up the existing repository.
2. Merge these files into the repository root. Do not delete your existing config files.
3. Replace the repository-root build.yaml with the build.yaml in this package.
4. Commit/push to GitHub and check Actions.
5. Only flash the resulting test_one UF2 if the build succeeds.

Important:
- This package has not been run through your repository's exact ZMK dependency versions, so the GitHub Actions build is the validation step.
- Pin naming assumes the board's D9 is exposed through the Pro Micro interconnect as &pro_micro 9.
- Connect the switch only between D9 and GND; do not connect D9 to VCC or RAW.
- If build fails, send the complete Actions error log before changing more files.
