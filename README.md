# APatch Modules Repository Example

[中文](docs/README_CN.md) | **English**

---

## Important Notes

- You may only upload **your own APatch modules**.  
  If you have explicit permission to upload a module developed by someone else, this is allowed, but **the uploader will be listed as the primary author**.
- All modules **must comply with applicable laws** and **must not perform malicious behavior**.
- The APatch Modules organization **does not provide warranty or technical support** for uploaded modules.
- Only the **default branch** of a repository will be indexed.

---

## Module Release Requirements

### Immutable Releases

For security and integrity, module repositories **must use immutable GitHub releases**:

- Git tags **must not be moved or deleted**
- Release assets **must not be modified or replaced**
- Each release **must represent exactly one version**

Immutable releases protect against:
- Release tampering
- Repository resurrection attacks

---

## Module Information

All module metadata **must** be declared in a `module.json` file located at the **repository root**.

> **`summary.en` and `description.en` are mandatory fields.**  
> Other languages are optional.

---

### Module Name *

The repository name and GitHub description.

---

### Module ID *

`moduleid` field in `module.json`.

Example:
"moduleid": "overlayfs-meta-module"

- Must be **globally unique**
- Must remain **unchanged across all versions**
- Recommended to match the repository name

---

### Meta Module *
"metamodule": true

- `true` → Meta module (dependency / capability check only)
- `false` → Functional module

---

### Summary (Required)

"summary": {
"en": "Meta module for OverlayFS support"
}

- **`summary.en` is required**
- Short, plain-text description
- Displayed in module lists
- No Markdown formatting
- Additional languages are optional

Multi-language example:

"summary": {
"en": "Meta module for OverlayFS support",
"ru": "Мета-модуль для поддержки OverlayFS"
}

---

### Description (Required)
"description": {
"en": "This meta module ensures that OverlayFS support is included in your kernel. OverlayFS allows you to create a unified filesystem by overlaying one filesystem on top of another, which is particularly useful for containerization and live systems."
}

- **`description.en` is required**
- Full module description
- Additional languages are optional

Multi-language example:
"description": {
"en": "This meta module ensures that OverlayFS support is included in your kernel.",
"ru": "Этот мета-модуль гарантирует, что поддержка OverlayFS включена."
}

---

### Homepage URL *

The repository homepage or support page  
(e.g. GitHub Issues).

---

### Source Code URL

"sourceUrl": "https://github.com/APatch-Modules/OverlayFS-Meta-Module"


- Optional
- Required if binaries are distributed but the source is hosted elsewhere

---

### Authors *

"authors": ["APatch Modules Team"]

- Primary authors of the module
- Individuals or organizations

---

### License *
"license": "GPL-2.0-only"

- Required
- Must be a valid **SPDX license identifier**

## Module Name

"modulename": "OverlayFS Meta Module"

- set module name

---

## Versions

"version": "1.0.0"

- Human-readable version string

---

### Version Code *
"VersionCode": 10000


- Integer only
- Must strictly increase with each release
- Used for update checks

---


### Changes

The GitHub release description **must** list:

- New features
- Bug fixes
- Behavior or compatibility changes

---

## Example module.json


{
"metamodule": true,
"summary": {
"en": "Meta module for OverlayFS support"
},
"description": {
"en": "This meta module ensures that OverlayFS support is included in your kernel. OverlayFS allows you to create a unified filesystem by overlaying one filesystem on top of another, which is particularly useful for containerization and live systems."
},
"sourceUrl": "https://github.com/APatch-Modules/OverlayFS-Meta-Module
",
"authors": ["APatch Modules Team"],
"license": "GPL-2.0-only",
"moduleid": "overlayfs-meta-module",
"version": "1.0.0",
"VersionCode": 10000
}