# React Native Developer Productivity Tool

Customer Guide for Windows EXE distribution.

This document is customer-facing only.
Internal/admin operations (build scripts, key generation, key signing, private-key handling) are intentionally excluded.

---

## English

### Product Summary

React Native Developer Productivity Tool is an offline CLI assistant for React Native CLI projects.
It helps you generate code, analyze project health, troubleshoot errors, and prepare releases faster.

### What You Receive

- `rn-tool.exe`
- `rn-tool-launcher.exe`
- License file (`.txt`) from seller

### System Requirements

- Windows 10/11
- React Native project source folder (for project analysis commands)
- Node.js/npm, Java, Android SDK (for environment/build related commands)
- Internet connection for some dependency checks

### Quick Start (Recommended: Launcher)

1. Put `rn-tool.exe`, `rn-tool-launcher.exe`, and your license `.txt` file in the same folder.
2. Double-click `rn-tool-launcher.exe`.
3. Type `f` (or `folder`) to choose your target React Native project folder.
4. Type `a` to auto-activate license from `.txt` in the same EXE folder.
5. Type `h` to see full help.
6. Type `r <number>` to run a quick command in the selected folder.

Launcher shortcuts:

- `f` or `folder`: choose target folder
- `a`: auto-activate license file in EXE folder
- `a <file>`: activate from a specific license file
- `v`: run `fix-error` using clipboard text
- `m`: paste multiline error logs, finish with `.end`
- `r <number>`: run a listed quick command
- `p` / `pwd` / `where`: print current working folder
- `l`: show quick command list
- `h`: help
- `q`: quit launcher

### Terminal Usage (Optional)

Show help:

```powershell
.\rn-tool.exe --help
```

Run command in current folder:

```powershell
.\rn-tool.exe --lang vi doctor
```

Run command with explicit project path:

```powershell
.\rn-tool.exe --lang en analyze -d "D:\reactnative\my-app"
```

If your EXE path contains spaces, use PowerShell call operator:

```powershell
& "C:\Tools\rn-tool\rn-tool.exe" --lang vi health -d "D:\reactnative\my-app"
```

### Language Settings

One-time language per command:

```powershell
rn-tool.exe --lang vi doctor
rn-tool.exe --lang en doctor
```

Save default language:

```powershell
rn-tool.exe config lang vi
rn-tool.exe config lang en
```

Quick alias:

```powershell
rn-tool.exe language vi
rn-tool.exe language en
```

Show current config:

```powershell
rn-tool.exe config show
```

### License Commands (Customer)

```powershell
rn-tool.exe license machine-id
rn-tool.exe license activate "<LICENSE_KEY>"
rn-tool.exe license activate-file ".\<license-file>.txt"
rn-tool.exe license status
rn-tool.exe license deactivate
```

If activation fails, send your `machine-id` to seller/support to receive the correct license file.

### Common Commands

| Command | Purpose |
|---|---|
| `rn-tool doctor` | Check environment readiness. |
| `rn-tool repair` | Auto-fix common environment/cache issues. |
| `rn-tool analyze` | Detect performance issues (rerender, memo, list, image size). |
| `rn-tool health` | Generate project health score/report. |
| `rn-tool check-deps` | Check dependency conflicts and risky updates. |
| `rn-tool map-navigation` | Visualize navigation tree/map. |
| `rn-tool detect-unused` | Find unused files/exports/assets. |
| `rn-tool fix-error [errorText...]` | Analyze build/runtime errors and suggest fixes. |
| `rn-tool create screen <name>` | Generate screen module boilerplate. |
| `rn-tool create component <name>` | Generate reusable component boilerplate. |
| `rn-tool create api <name>` | Generate API service boilerplate. |
| `rn-tool create store <name>` | Generate store boilerplate. |
| `rn-tool prepare-release` | Run release-readiness checklist. |

### Recommended Workflow

1. `rn-tool doctor`
2. `rn-tool check-deps`
3. `rn-tool analyze`
4. `rn-tool health`
5. `rn-tool map-navigation`
6. `rn-tool detect-unused`
7. `rn-tool prepare-release`

### Notes

- Use `--lang en` or `--lang vi` for output language.
- `build-ios` requires macOS + Xcode environment.
- Keep your license file private and do not share it publicly.

---

## Tieng Viet

### Tong quan

React Native Developer Productivity Tool la CLI offline danh cho du an React Native CLI.
Cong cu giup tao boilerplate nhanh, phan tich chat luong du an, ho tro sua loi, va chuan bi release.

### Goi file khach hang nhan

- `rn-tool.exe`
- `rn-tool-launcher.exe`
- File license (`.txt`) do ben ban cung cap

### Yeu cau he thong

- Windows 10/11
- Thu muc source du an React Native (de chay cac lenh phan tich)
- Node.js/npm, Java, Android SDK (cho cac lenh lien quan moi truong/build)
- Internet cho mot so lenh kiem tra dependency

### Bat dau nhanh (Khuyen nghi: Launcher)

1. Dat `rn-tool.exe`, `rn-tool-launcher.exe`, va file license `.txt` cung mot thu muc.
2. Nhan dup `rn-tool-launcher.exe`.
3. Nhap `f` (hoac `folder`) de chon thu muc du an React Native.
4. Nhap `a` de tu dong kich hoat license tu file `.txt` cung thu muc EXE.
5. Nhap `h` de xem huong dan day du.
6. Nhap `r <so>` de chay nhanh lenh trong folder da chon.

Phim tat launcher:

- `f` hoac `folder`: chon thu muc du an
- `a`: tu dong kich hoat license trong thu muc EXE
- `a <file>`: kich hoat tu file license chi dinh
- `v`: chay `fix-error` bang noi dung clipboard
- `m`: paste log loi nhieu dong, ket thuc bang `.end`
- `r <so>`: chay nhanh mot lenh trong danh sach
- `p` / `pwd` / `where`: in lai thu muc hien tai
- `l`: hien danh sach lenh nhanh
- `h`: xem help
- `q`: thoat launcher

### Su dung bang terminal (Tuy chon)

Xem help:

```powershell
.\rn-tool.exe --help
```

Chay trong thu muc hien tai:

```powershell
.\rn-tool.exe --lang vi doctor
```

Chay voi duong dan du an cu the:

```powershell
.\rn-tool.exe --lang en analyze -d "D:\reactnative\my-app"
```

Neu duong dan co dau cach, dung call operator:

```powershell
& "C:\Tools\rn-tool\rn-tool.exe" --lang vi health -d "D:\reactnative\my-app"
```

### Cai dat ngon ngu

Doi ngon ngu cho tung lenh:

```powershell
rn-tool.exe --lang vi doctor
rn-tool.exe --lang en doctor
```

Dat ngon ngu mac dinh:

```powershell
rn-tool.exe config lang vi
rn-tool.exe config lang en
```

Alias nhanh:

```powershell
rn-tool.exe language vi
rn-tool.exe language en
```

Xem cau hinh hien tai:

```powershell
rn-tool.exe config show
```

### Lenh license (Danh cho khach hang)

```powershell
rn-tool.exe license machine-id
rn-tool.exe license activate "<LICENSE_KEY>"
rn-tool.exe license activate-file ".\<ten-file-license>.txt"
rn-tool.exe license status
rn-tool.exe license deactivate
```

Neu kich hoat that bai, gui `machine-id` cho ben ban/support de duoc cap lai file license dung.

### Lenh thong dung

| Lenh | Muc dich |
|---|---|
| `rn-tool doctor` | Kiem tra san sang moi truong. |
| `rn-tool repair` | Tu dong sua loi moi truong/cache pho bien. |
| `rn-tool analyze` | Phat hien van de hieu nang (rerender, memo, list, image size). |
| `rn-tool health` | Tao diem suc khoe tong the cua du an. |
| `rn-tool check-deps` | Kiem tra xung dot/rui ro dependency. |
| `rn-tool map-navigation` | Ve tong quan navigation tree/map. |
| `rn-tool detect-unused` | Tim file/export/asset khong su dung. |
| `rn-tool fix-error [errorText...]` | Phan tich loi va goi y cach sua. |
| `rn-tool create screen <name>` | Tao boilerplate module screen. |
| `rn-tool create component <name>` | Tao boilerplate component tai su dung. |
| `rn-tool create api <name>` | Tao boilerplate API service. |
| `rn-tool create store <name>` | Tao boilerplate store. |
| `rn-tool prepare-release` | Chay checklist truoc release. |

### Quy trinh de xuat

1. `rn-tool doctor`
2. `rn-tool check-deps`
3. `rn-tool analyze`
4. `rn-tool health`
5. `rn-tool map-navigation`
6. `rn-tool detect-unused`
7. `rn-tool prepare-release`

### Ghi chu

- Dung `--lang en` hoac `--lang vi` de chon ngon ngu output.
- `build-ios` can moi truong macOS + Xcode.
- Khong chia se cong khai file license.