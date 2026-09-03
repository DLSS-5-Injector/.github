# 🎮 DLSS 5 Injector

Wrapper DLL injector designed to enable and configure **DLSS 5** features in compatible games, with support for advanced DLSS overrides, model selection, scaling controls, and image-quality tweaks.

---

## 🔗 Get the Latest Release

- [📦 View All Releases]()

---

## ✨ DLSS 5 Support

**DLSS 5** features can be enabled in supported titles through the injector and its configuration system.

Depending on the game and installed NVIDIA DLSS version, available options may include:

- DLSS 5 model overrides
- Transformer model selection
- DLAA forcing
- Custom DLSS scaling ratios
- DLSS preset overrides
- Advanced rendering configuration

> **Note:** DLSS 5 functionality depends on the game's DLSS implementation and installed NVIDIA DLSS runtime. Not every title will support every feature.

---

# 🚀 Setup

Most compatible games can be configured in just a few steps.

## 1. Download

Download the latest release ZIP and extract it next to the game's main executable.

> **Note:** The executable may be located inside a subfolder. For Unreal Engine games, it is commonly named:
>
> ```text
> GameName-Win64-Shipping.exe
> ```

## 2. Run the Configuration Tool

Launch:

```text
DLSS5InjectorConfig.exe
```

The configuration utility will detect available injector options and allow you to configure the desired DLSS settings.

If required, the tool may prompt you to enable the NVIDIA signature override required by certain injection methods.

## 3. Configure DLSS 5

Select the features you want to enable.

Common options include:

- Enable **DLSS 5**
- Force **DLAA**
- Override DLSS presets
- Select supported Transformer models
- Configure custom scaling ratios
- Enable advanced rendering options

Hover over individual settings inside the configuration tool for additional information.

## 4. Save & Launch

Save your configuration and start the game.

If the injector loads successfully, a log file should be generated next to the game's executable:

```text
dlss5injector.log
```

The log can be used to verify that the injector and DLSS runtime were successfully detected.

---

# ⚠️ Compatibility

Compatibility depends on the game, NVIDIA DLSS version, rendering API, and the method used to load the injector.

Games using newer DLSS runtimes may require a different wrapper DLL than older titles.

Games originally released with older DLSS implementations may continue to work after updating their DLSS runtime, although compatibility is not guaranteed.

> **Important:** DLSS 5 features are only available when the underlying game and installed DLSS runtime expose the required functionality.

---

# 🛠 Automatic Installation

The configuration utility can automatically select and install a compatible wrapper DLL.

### Installation

1. Extract the injector somewhere outside the game directory.
2. Run:

```text
DLSS5InjectorConfig.exe
```

3. Select:

```text
Copy to Game Folder
```

4. Select the game's installation directory.

The configuration tool will attempt to identify a compatible wrapper filename and copy the required files automatically.

---

# 🔧 Advanced Setup

## Alternate DLL Wrapper Filenames

Depending on the game, the injector may be loaded through one of several supported wrapper DLL names:

```text
XInput1_3.dll
XInput1_4.dll
XInput9_1_0.dll
dxgi.dll
XAPOFX1_5.dll
X3DAudio1_7.dll
winmm.dll
```

### Recommended Wrappers

The following wrappers generally provide the highest compatibility:

```text
dxgi.dll
winmm.dll
XInput1_3.dll
XInput1_4.dll
```

If the injector does not load using one filename, try another supported wrapper.

If none of the supported wrappers work, please report the game and its rendering API so compatibility can be investigated.

---

# ⚙️ Direct `nvngx.dll` Wrapping

The injector can optionally wrap the NVIDIA DLSS module directly by using:

```text
nvngx.dll
```

This method can provide compatibility with titles where conventional wrapper DLL injection does not work.

However, compatibility may vary depending on the installed NVIDIA DLSS version and the game's implementation.

### NVIDIA Signature Override

Certain direct-wrapping configurations may require NVIDIA DLL signature verification to be disabled.

The configuration utility can apply the required registry modification automatically.

Alternatively, the included registry file can be used:

```text
EnableNvidiaSigOverride.reg
```

To restore the original configuration:

```text
DisableNvidiaSigOverride.reg
```

> **Warning:** Only use signature-override functionality if you understand the implications of modifying NVIDIA's DLL verification behavior.

---

# ⚠️ Online Games & Anti-Cheat

The use of DLL wrappers, runtime injection, or direct `nvngx.dll` wrapping may conflict with anti-cheat systems.

Some anti-cheat software may interpret DLL injection or code-hooking behavior as suspicious, even when the injector itself does not modify gameplay.

**Do not use this injector with competitive or protected online games unless you have confirmed that modifications are permitted.**

Use at your own risk.

---

# 🗑 Uninstalling

To remove the DLSS 5 Injector:

1. Close the game.
2. Remove the injector files from the game directory.
3. Delete the installed wrapper DLL, such as:

```text
dxgi.dll
winmm.dll
XInput1_3.dll
XInput1_4.dll
nvngx.dll
```

4. If the NVIDIA signature override was enabled, restore the original configuration using:

```text
DisableNvidiaSigOverride.reg
```

5. Restart the system if required.

---

# 📋 Troubleshooting

| Issue | Solution |
| --- | --- |
| Injector does not load | Try a different supported wrapper filename |
| No log file is generated | Verify that the injector files are next to the game executable |
| Game crashes on startup | Restore default settings and disable custom DLSS overrides |
| DLSS 5 does not activate | Confirm that the game and installed DLSS runtime support the required functionality |
| DLAA does not activate | Verify that the game supports DLSS/DLAA |
| Settings are ignored | Check the injector configuration and selected wrapper |
| Game stops launching after installation | Remove the wrapper DLL and restore the original game files |
| Anti-cheat warning appears | Remove the injector and do not use it with the affected online title |

---

# 🧪 Compatibility Reporting

When reporting an incompatible game, please include:

```text
Game:
Game Version:
GPU:
Windows Version:
DLSS Version:
Rendering API:
Wrapper DLL:
Injector Version:
Crash / Error:
Log File:
```

Providing the `dlss5injector.log` file is highly recommended when troubleshooting.

---

# ⚠️ Disclaimer

DLSS 5 Injector is provided for personal customization, testing, and experimentation.

Always back up original game files before installing modifications.

The developers are not responsible for:

- Game crashes
- Corrupted files
- Lost saves
- Performance issues
- System instability
- Anti-cheat actions
- Account restrictions
- Compatibility problems
- Damage resulting from improper configuration

Use the software at your own risk.

---

# ❤️ Support Development

If you find DLSS 5 Injector useful, consider supporting future development and compatibility testing.

Support helps with:

- New DLSS runtime compatibility
- Game testing
- Injector improvements
- New configuration options
- Bug fixes
- Compatibility research

Thank you for supporting the project!

---

# 📜 Distribution

Please do **not** re-upload DLSS 5 Injector or modified builds to third-party websites.

Link to the official project page instead so users can always obtain the latest version and verify the authenticity of the release.

---

# 📄 License

See [`LICENSE`](LICENSE) for the terms under which DLSS 5 Injector is distributed.
