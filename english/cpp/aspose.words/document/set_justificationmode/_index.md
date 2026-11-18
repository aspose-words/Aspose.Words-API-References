---
title: Aspose::Words::Document::set_JustificationMode method
linktitle: set_JustificationMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::set_JustificationMode method. Sets the character spacing adjustment of a document in C++.'
type: docs
weight: 162000
url: /cpp/aspose.words/document/set_justificationmode/
---
## Document::set_JustificationMode method


Sets the character spacing adjustment of a document.

```cpp
void Aspose::Words::Document::set_JustificationMode(Aspose::Words::Settings::JustificationMode value)
```

## Examples


Shows how to manage character spacing control.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Document.docx"));

Aspose::Words::Settings::JustificationMode justificationMode = doc->get_JustificationMode();
if (justificationMode == JustificationMode::Expand)
{
    doc->set_JustificationMode(JustificationMode::Compress);
}

doc->Save(get_ArtifactsDir() + u"Document.SetJustificationMode.docx");
```
## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
