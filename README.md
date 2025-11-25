# Ironless-QDD-Actuator

## Overview

The Ironless-QDD-Actuator is a low-cost, high-torque, fully 3D-printed quasi-direct-drive actuator for robotics projects. Using a Halbach array for an ironless rotor and a 3D-printed cycloidal planetary gearbox, it delivers up to 29.4Nm of holding torque for \~$70 (with controller). All custom parts are 3D-printable, making it ideal for makers and hobbyists.

### Key Features

- **Low Cost**: \~$40 (actuator), \~$70 (with controller)
- **High Torque**: 29.4Nm holding torque
- **Fully 3D-Printed**: No machining required
- **Ironless Rotor**: Halbach array for high efficiency
- **Zero Backlash**: Cycloidal gearbox for precision

## Documentation

For detailed design, assembly, and testing info, see my blog post:\
https://cadenkraft.com/ironless-cycloidal-planetary-actuator/

## Repository Contents

- CAD files for entire actuator
- FEMM simulation files
- Bill of Materials (BOM)
- ODrive configuration for MKS X Drive

## Assembly Tips

- USE ENGINEERING PLASTICS! (PA6-GF, PA6-CF, PET-CF, etc) Using PLA is tempting but the rotor will definilty creep due to the magnetic forces.
- Rotor specifically needs to be printed @ 100% infill using a high stiffness plastic with low creep
- Using "CF-Core" filaments for the gears is untested but should work amazingly for having the smooth non abrasive plastic on the outside but still having the stiff carbon additives for strength
- M3 Tap is needed for assembling the planet carrier
- Lithium grease should be used inside the gearbox assembly

## License

MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this project and associated files to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies, provided the following notice is included:

Credit: Caden Kraft (GitHub: CKraft11)

## Contributing

Feedback and contributions are welcome! Submit issues or pull requests on GitHub. If you use this actuator, please share your project!

## Git LFS Required

This repository tracks large binary assets (e.g., `.STEP` CAD files and FEMM outputs) with Git Large File Storage (LFS). To clone and receive these files correctly, install Git LFS before cloning.

If you hit LFS bandwidth limits, the full print and CAD files are also mirrored on MakerWorld: https://makerworld.com/en/models/2042262-caden-kraft-s-qdd-cycloidal-planetary-actuator#profileId-2203426

- Install Git LFS:
  - Windows: `winget install Git.GitLFS` or install via Git for Windows installer (enable LFS component)
  - macOS: `brew install git-lfs`
  - Linux: `sudo apt-get install git-lfs` (Debian/Ubuntu) or use your distro’s package manager
- Initialize LFS once on your machine: `git lfs install`
- Clone the repo: `git clone https://github.com/CKraft11/Ironless-QDD-Actuator.git`

If you already cloned without LFS and see small pointer files instead of the actual binaries, run:

- Ensure LFS is installed: `git lfs install`
- Fetch LFS content: `git lfs fetch --all`
- Checkout LFS files: `git lfs checkout`
  - If needed to fully rehydrate files: `git rm --cached -r .` then `git reset --hard`

Notes
- You do not need to run `git lfs track` yourself; the repository already contains `.gitattributes` with the correct patterns.
- When contributing changes to large binaries, commit as usual; LFS handles storage automatically once installed.

