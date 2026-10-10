---
title: "Aspose::Words::Document::get_JustificationMode 方法"
linktitle: "get_JustificationMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_JustificationMode 方法。获取或设置文档的字符间距调整（C++）。"
type: docs
weight: 34000
url: /zh/cpp/aspose.words/document/get_justificationmode/
---
## Document::get_JustificationMode method


获取或设置文档的字符间距调整。

```cpp
Aspose::Words::Settings::JustificationMode Aspose::Words::Document::get_JustificationMode()
```


## 示例



展示如何管理字符间距控制。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

Aspose::Words::Settings::JustificationMode justificationMode = doc->get_JustificationMode();
if (justificationMode == Aspose::Words::Settings::JustificationMode::Expand)
{
    doc->set_JustificationMode(Aspose::Words::Settings::JustificationMode::Compress);
}

doc->Save(get_ArtifactsDir() + u"Document.SetJustificationMode.docx");
```

## 另见

* Enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
