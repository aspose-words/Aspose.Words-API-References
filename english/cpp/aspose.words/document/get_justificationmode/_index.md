---
title: Aspose::Words::Document::get_JustificationMode method
linktitle: get_JustificationMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_JustificationMode method. Gets or sets the character spacing adjustment of a document in C++.'
type: docs
weight: 34000
url: /cpp/aspose.words/document/get_justificationmode/
---
## Document::get_JustificationMode method


Gets or sets the character spacing adjustment of a document.

```cpp
Aspose::Words::Settings::JustificationMode Aspose::Words::Document::get_JustificationMode()
```


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

* Enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
