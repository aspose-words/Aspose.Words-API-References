---
title: Aspose::Words::Settings::JustificationMode enum
linktitle: JustificationMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Settings::JustificationMode enum. Specifies the character spacing adjustment for a document. The default value is Expand in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words.settings/justificationmode/
---
## JustificationMode enum


Specifies the character spacing adjustment for a document. The default value is **Expand**.

```cpp
enum class JustificationMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Expand | 0 | Do not compress character spacing. |
| Compress | 1 | Compress character spacing. |
| CompressKana | 2 | Compress, using rules of the kana syllabaries, Hiragana and Katakana. |


## Examples



Shows how to manage character spacing control. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

Aspose::Words::Settings::JustificationMode justificationMode = doc->get_JustificationMode();
if (justificationMode == Aspose::Words::Settings::JustificationMode::Expand)
{
    doc->set_JustificationMode(Aspose::Words::Settings::JustificationMode::Compress);
}

doc->Save(get_ArtifactsDir() + u"Document.SetJustificationMode.docx");
```

## See Also

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
