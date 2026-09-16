---
title: "Aspose::Words::EditorType enum"
linktitle: "EditorType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::EditorType 枚举。指定一组可能的别名（或编辑组），可用作别名来确定当前用户是否被允许在 C++ 中编辑文档内由可编辑范围定义的单个范围。"
type: docs
weight: 88000
url: /zh/cpp/aspose.words/editortype/
---
## EditorType enum


指定一组可能的别名（或编辑组），可用作别名以确定当前用户是否被允许编辑文档中由可编辑范围定义的单个范围。

```cpp
enum class EditorType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 未指定 | 0 | 表示未指定编辑器类型。 |
| 管理员 | 1 | 指定当启用文档保护时，属于 Administrators 组的用户将被允许使用此编辑类型编辑可编辑范围。 |
| 贡献者 | 2 | 指定当启用文档保护时，属于 Contributors 组的用户将被允许使用此编辑类型编辑可编辑范围。 |
| 当前 | 3 | 指定当启用文档保护时，属于 Current 组的用户将被允许使用此编辑类型编辑可编辑范围。 |
| 编辑者 | 4 | 指定当启用文档保护时，属于 Editors 组的用户将被允许使用此编辑类型编辑可编辑范围。 |
| 所有人 | 5 | 指定当启用文档保护时，打开文档的所有用户将被允许使用此编辑类型编辑可编辑范围。 |
| None | 6 | 指定当启用文档保护时，打开文档的用户均不被允许使用此编辑类型编辑可编辑范围。 |
| 所有者 | 7 | 指定当启用文档保护时，属于 Owners 组的用户将被允许使用此编辑类型编辑可编辑范围。 |
| Default | n/a | 同 [Unspecified](./) 一样。 |

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
