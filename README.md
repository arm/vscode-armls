# ArmLS for Visual Studio Code

A Visual Studio Code extension that provides language support for Arm Assembly by means of the [ArmLS](https://github.com/arm/armls) language server.

## Features

- Hover support for instructions and operands
- Semantic highlighting
- Completion sourced from mnemonics, labels, set directives, and macros
- Real-time diagnostics with customizable configuration and support for `clang`
- Document symbols (goto definition and document symbols)

## Configuration

You can configure this extension through the **Settings** page in VS Code.

1. Press `Ctrl+,` to open the **Settings** page.
1. Search for "ArmLS".

### Configure diagnostics

To disable particular diagnostic categories, use the Armls › Diagnostics: **Disable Categories** setting.

To configure whether ArmLS provides validation diagnostics to VS Code, use the **Armls: Enable Diagnostics** setting.

To configure external diagnostics by means of a `clang` binary:
1. Use the ArmLS > External Diagnostics > clang: **Path** setting to specify the path to the `clang` executable file.
1.  Use the ArmLS > External Diagnostics > clang: **Args** setting to specify any arguments.


## Contact

To report bugs or request enhancements, use the [ArmLS](https://github.com/arm/armls) repository's GitHub [issues](https://github.com/arm/armls/issues).
