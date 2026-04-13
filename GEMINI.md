# Star Citizen Localization Distribution (sc-translation-pack)

This repository serves as the distribution and publication layer for the *Star Citizen* Traditional Chinese localization project. It contains the final `.ini` files consumed by players and the automation for releasing new versions.

## Directory Overview

This is a **Non-Code (Data/Asset) Project**. It acts as the "output" repository for the [star-citizen-loc](https://github.com/cosmo-chang-1701/star-citizen-loc) translation engine.

- **Purpose**: To provide high-quality, AI-refined Traditional Chinese translations for *Star Citizen*.
- **Mechanism**: LLM-powered translation refined for context and game-specific terminology.
- **Distribution**: Automated via GitHub Actions (Releases) and Discord notifications.

## Key Files

- **`chinese_(traditional)/global.ini`**: The core localization file. This is a massive key-value pair file (`KEY=Value`) used by the game engine.
- **`.github/workflows/release.yml`**:
    - Triggers on tags matching `v*.*.*-v*` (e.g., `v4.6.0-v1`).
    - Packages the translation into a ZIP file.
    - Creates a GitHub Release with auto-generated notes and comparison links.
    - Sends a notification to the Star Netrunners Discord.
- **`README.md`**: Provides end-user installation instructions (manual and Git-based).
- **`LICENSE`**: CC BY-NC-SA 4.0 International.

## Usage & Workflow

### For Players
Players should download the latest release from the [Releases](https://github.com/cosmo-chang-1701/sc-translation-pack/releases) page and extract the `global.ini` to their game's `Localization` folder.

### For Developers (Ecosystem Context)
This repository is the final stage of a three-part system:
1.  **[star-citizen-fine-tune-model](../star-citizen-fine-tune-model)**: Fine-tunes Qwen2.5 models on game-specific datasets.
2.  **[star-citizen-loc](..)**: The translation engine that uses the fine-tuned model to process raw English `.ini` files into this directory.
3.  **sc-translation-pack (This Repo)**: The public-facing repository where results are committed and released.

### Releasing a New Version
To trigger an official release:
1. Tag the repository: `git tag v[GameVersion]-v[PackVersion]` (e.g., `git tag v4.0.0-v1.0.1`).
2. Push the tag: `git push origin v4.0.0-v1.0.1`.
3. The GitHub Action will automatically package the files, create the release, and notify the Discord community.

## Technical Standards

- **File Encoding**: The `global.ini` file should be standard UTF-8.
- **Format Consistency**: Strictly maintain the `KEY=Value` format. Keys may include game-engine suffixes like `,P`.
- **Integrity**: Only text-based localization files are allowed; no modifications to game executables.
