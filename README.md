# TIA Portal Siemens Library

A Siemens TIA Portal V21 library collection for reusable PLC control blocks.

This repository keeps both ready-to-import TIA library archives and source-style exports for review and version tracking.

## Contents

```text
archives/
  FlowControl.zal21
  FlowControl-v0.1.1.zal21
  MotionControl.zal21

blocks/
  xml/
    FlowControl_LAD.xml
    FlowControl_SCL.xml
    MotionControl_LAD.xml
  udt/
    UDT_FlowControl.udt
    UDT_FlowControl-v0.1.1.udt
    UDT_MotionControl.udt

libraries/
  FlowControl/
    FlowControl.al21
    LibraryInfo.txt
    ...
  FlowControl-v0.1.1/
    FlowControl-v0.1.1.al21
    LibraryInfo.txt
    ...
  MotionControl/
    MotionControl_LAD.al21
    LibraryInfo.txt
    ...
```

## Directory Guide

### `archives/`

Compressed TIA Portal global library archives.

Use these when you want the simplest import path in TIA Portal.

### `libraries/`

Expanded TIA Portal global library folders.

These folders intentionally include TIA internal folders such as `System`, `TMP`, `Vci`, `XRef`, `IM`, and `AdditionalFiles`. Do not delete or ignore these folders when you want the `.al21` library to remain openable in TIA Portal.

### `blocks/xml/`

XML exports of PLC blocks. These files are the best place to review changes in GitHub.

### `blocks/udt/`

PLC data type source files used by the libraries.

## Usage

1. Download the latest `.zal21` file from `archives/` or the GitHub Release page.
2. Open TIA Portal V21.
3. Open the global library or retrieve the archive.
4. Drag the required blocks or types into your PLC project.

## Notes

- The libraries are intended for TIA Portal V21.
- `FlowControl-v0.1.1` updates the FlowControl UDT interface names to the `i_` and `o_` naming style.
- Keep XML exports in Git for easier diff and review.
- Keep `.zal21` archives for convenient reuse.
- Keep expanded `.al21` library folders complete. Their internal folders are part of the TIA library structure.

## 中文说明

这个仓库用于保存西门子 TIA Portal V21 可复用 PLC 库，包括：

- `.zal21` 全局库归档，方便下载和导入。
- 展开后的 `.al21` 全局库目录，方便直接打开和版本跟踪。
- FB/FC 等块的 XML 导出文件，方便在 GitHub 查看差异。
- UDT 数据类型源文件。

注意：`libraries/` 下面的 `System`、`TMP`、`Vci`、`XRef`、`IM` 等目录不要删除，它们是 TIA 展开库结构的一部分。
