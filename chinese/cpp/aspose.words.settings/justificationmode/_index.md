---
title: "Aspose::Words::Settings::JustificationMode enum"
linktitle: "JustificationMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::JustificationMode enum. 指定文档的字符间距调整。默认值是 C++ 中的 Expand。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.settings/justificationmode/
---
## JustificationMode enum


指定文档的字符间距调整。默认值为 **Expand**。

```cpp
enum class JustificationMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Expand | 0 | 不要压缩字符间距。 |
| Compress | 1 | 压缩字符间距。 |
| CompressKana | 2 | 压缩，使用假名音节表（平假名和片假名）的规则。 |


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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
