# Third-party notices

The Windows build bundles the following components under their own licences. The full texts
ship inside the app at `desktop/web/licenses.html` (served at `/licenses.html` by the receiver)
and are regenerated whenever the Python runtime is updated.

| Component | Licence | Where |
|---|---|---|
| Python 3.13 runtime and standard library | PSF License | `_internal/python313.dll`, `_internal/*.pyd` |
| Tcl/Tk 8.6 | Tcl/Tk licence (BSD-style) | `_internal/_tcl_data`, `_internal/_tk_data`, `tcl86t.dll`, `tk86t.dll` |
| PyInstaller bootloader and runtime hooks | GPL 2.0 with the bootloader exception (permits proprietary apps) | `Virtual SFX Lab.exe` stub |
| Microsoft Visual C++ runtime | Microsoft redistributable licence | `_internal/VCRUNTIME140*.dll` (left with Microsoft's signature) |
| chess.js | BSD 2-Clause, Copyright (c) 2025 Jeff Hlywa | `desktop/web/vendor/chess.js`, `desktop/web/vendor/chess.LICENSE` |

Web fonts are not bundled; the Windows build uses the system font stack.
