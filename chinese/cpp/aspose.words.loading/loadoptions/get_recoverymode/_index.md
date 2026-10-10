---
title: "Aspose::Words::Loading::LoadOptions::get_RecoveryMode 方法"
linktitle: "get_RecoveryMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::LoadOptions::get_RecoveryMode 方法。定义在加载期间出现错误时文档应如何处理。使用此属性指定系统是应尝试恢复文档还是遵循其他定义的行为。默认值在 C++ 中为 TryRecover。"
type: docs
weight: 14500
url: /zh/cpp/aspose.words.loading/loadoptions/get_recoverymode/
---
## LoadOptions::get_RecoveryMode method


定义在加载期间出现错误时文档应如何处理。使用此属性指定系统是应尝试恢复文档还是遵循其他定义的行为。默认值为 [TryRecover](../../documentrecoverymode/)。

```cpp
Aspose::Words::Loading::DocumentRecoveryMode Aspose::Words::Loading::LoadOptions::get_RecoveryMode() const
```


## 示例



展示在加载期间出现错误时如何尝试恢复文档。
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_RecoveryMode(Aspose::Words::Loading::DocumentRecoveryMode::TryRecover);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Corrupted footnotes.docx", loadOptions);
```

## 另见

* Enum [DocumentRecoveryMode](../../documentrecoverymode/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
