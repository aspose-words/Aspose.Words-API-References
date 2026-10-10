---
title: "Aspose::Words::Loading::DocumentRecoveryMode enum"
linktitle: "DocumentRecoveryMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::DocumentRecoveryMode 枚举。指定当文档在 C++ 中加载时遇到错误时可用的恢复选项。"
type: docs
weight: 13500
url: /zh/cpp/aspose.words.loading/documentrecoverymode/
---
## DocumentRecoveryMode enum


指定文档在加载期间遇到错误时可用的恢复选项。

```cpp
enum class DocumentRecoveryMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 不尝试恢复。如果文档无效，加载将因错误而失败。 |
| TryRecover | 1 | 尝试恢复文档，同时尽可能保留更多数据。 |


## 示例



展示在加载期间出现错误时如何尝试恢复文档。
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## 另见

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
