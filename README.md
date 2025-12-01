# ArmLS for Visual Studio Code

A Visual Studio Code extension that provides language support for Arm Assembly by means of the [ArmLS](https://github.com/arm/armls) language server.

In addition to syntax highlighting, this extension offers rich editor features including on-hover documentation and go-to-definition.

## Features

- Syntax highlighting

  ![The start of a aarch64 memcpy implementation, which is syntax highlighted](https://github.com/ARM/vscode-armls/raw/main/docs/images/hero-memcpy.png)
- Hover support for instructions and operands:

  ![AESD - AES single round decryption
    Requires: FEAT_AES
    Operands:
    1 - Vd: Register
    2 - 16B: ArrangementSpecifier
    3 - Vn: Register
    4 - 16B: ArrangementSpecifier
    AES single round decryption.](https://github.com/ARM/vscode-armls/raw/main/docs/images/hover.png)
- Completion sourced from mnemonics, labels, set directives, and macros

  ![A video of editing code. I starts with a label 'infinate_loop:'. The user types 'b in' and a suggestion to complete to 'infinate_loop' comes up. The user accepts the suggestion](https://github.com/ARM/vscode-armls/raw/main/docs/images/completion.gif)
- Document symbols (goto definition and document symbols)

  ![A video of some code. The user right clicks on a label referenced in an instruction, and click 'Go to defintion', and goes to where the label is defined](https://github.com/ARM/vscode-armls/raw/main/docs/images/goto-def.gif)
- Real-time diagnostics with customizable configuration and support for `clang`

  ![Some code 'b label, label'. The second 'label' has a red highlight, and a diagnostic saying 'invalid operand for instruction' from 'armls(clang)'](https://github.com/ARM/vscode-armls/raw/main/docs/images/clang-diagnostic.png)

## Supported Architecture

Armv9.6-A, both A32 and A64.

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

## Current limitations

ArmLS is in preview and has the current limitations:

- No support for cross-file references
- No support for C/C++ pre-processor syntax
- The internal diagnostics engine is alpha quality and might display false positives. We recommend that you use `clang`-powered diagnostics at this time.
- A32 only supports 
  [Unified Assembler Language](https://developer.arm.com/documentation/101754/0624/armasm-Legacy-Assembler-Reference/Writing-A32-T32-Instructions-in-armasm-Syntax-Assembly-Language/About-the-Unified-Assembler-Language)
  ([`.syntax unified`](https://sourceware.org/binutils/docs-2.45/as/ARM_002dInstruction_002dSet.html))


## Contact

To report bugs or request enhancements, use the [ArmLS](https://github.com/arm/armls) repository's GitHub [issues](https://github.com/arm/armls/issues).
