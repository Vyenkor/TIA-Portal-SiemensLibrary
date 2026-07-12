# TIA Portal Siemens Library

A Siemens TIA Portal V21 library collection for reusable PLC control blocks.

This repository keeps ready-to-import TIA library archives, expanded global libraries, XML block exports, and UDT source files for review and version tracking.

## Contents

```text
archives/
  FlowControl/
    FlowControl.zal21
    FlowControl-v0.1.1.zal21
    FlowControl-v0.1.2.zal21
    FlowControl-v0.1.3.zal21
  MotionControl/
    MotionControl.zal21
    MotionControl-v0.1.1.zal21
  SingleSolCyl/
    SingleSolCyl.zal21

blocks/
  xml/
    FlowControl/
    MotionControl/
    SingleSolCyl/
  udt/
    UDT_FlowControl/
    UDT_MotionControl/

libraries/
  FlowControl/
    FlowControl/
    FlowControl-v0.1.1/
    FlowControl-v0.1.2/
    FlowControl-v0.1.3/
  MotionControl/
    MotionControl/
    MotionControl-v0.1.1/
  SingleSolCyl/
    SingleSolCyl/
```

## Directory Guide

### `archives/`

Compressed TIA Portal global library archives, grouped by library name.

Use these when you want the simplest import path in TIA Portal.

### `libraries/`

Expanded TIA Portal global library folders, grouped by library name and version.

These folders intentionally include TIA internal folders such as `System`, `TMP`, `Vci`, `XRef`, `IM`, and `AdditionalFiles`. Do not delete or ignore these folders when you want the `.al21` library to remain openable in TIA Portal.

### `blocks/xml/`

TIA Openness XML exports of PLC blocks. These files are the best place to review behavior changes in GitHub.

### `blocks/udt/`

PLC data type source files used by the libraries.

## Usage

1. Download the required `.zal21` file from `archives/` or the GitHub Release page.
2. Open TIA Portal V21.
3. Open the global library or retrieve the archive.
4. Drag the required blocks or types into your PLC project.

## Notes

- The libraries are intended for TIA Portal V21.
- `FlowControl` now includes base, `v0.1.1`, `v0.1.2`, and `v0.1.3` exports.
- `MotionControl` now includes base and `v0.1.1` exports.
- `SingleSolCyl` has archive, expanded library, and LAD/SCL XML block exports.
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
