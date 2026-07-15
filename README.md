# Steamless-hwa

Steamless is a DRM remover for SteamStub DRM, originally developed by atom0s. This repository (`Steamless-hwa`) is a fork maintained by **화영왕 (Hwa-young-wang)**.

Steamless aims to unpack SteamStub DRM from compiled executables (PE32/PE64) to allow for easier reverse engineering and modding.

---

## 🚀 Features

- **SteamStub DRM Removal**: Supports unpacking SteamStub versions 1.x, 2.x, and 3.x (both x86 and x64 variants).
- **GUI and CLI Support**: Comes with a user-friendly WPF-based graphical user interface (`Steamless`) and a command-line interface (`Steamless.CLI`).
- **Extensible Plugin Architecture**: Easily extend unpacker variants and custom decryption modules using the Plugin API.

---

## 🛠️ Project Structure

- **Steamless**: The main WPF desktop application.
- **Steamless.CLI**: Command-line interface for automated workflows.
- **Steamless.API**: Core API for creating plugins and custom unpackers.
- **Steamless.Unpacker.Variant***: Default unpacker variants included with Steamless.
- **ExamplePlugin**: An example plugin demonstrating how to use the Steamless API.

---

## 💻 Requirements

- **.NET Framework 4.8** or higher
- Windows OS (WPF is used for the GUI)

---

## ⚙️ Building the Project

1. Open `Steamless.sln` in **Visual Studio 2022** (or higher).
2. Set the build configuration to `Release` and target platform to `Any CPU` / `x86` / `x64`.
3. Restore NuGet packages if prompted.
4. Build the solution.

---

## 📜 Usage

### GUI (Steamless)
1. Run `Steamless.exe`.
2. Browse or drag-and-drop the target SteamStub-protected executable.
3. Configure unpack options (e.g. keep section headers, bind imports, etc.).
4. Click **Unpack File**. The unpacked executable will be saved in the same directory with `.unpacked` appended to the filename.

### CLI (Steamless.CLI)
Run the CLI from the command prompt or terminal:
```cmd
Steamless.CLI.exe --file <path_to_executable> [options]
```

---

## 🤝 Credits & Acknowledgements

- **atom0s**: The original developer of Steamless.
- Contributors and reverse engineers who analyzed the SteamStub DRM variants.
