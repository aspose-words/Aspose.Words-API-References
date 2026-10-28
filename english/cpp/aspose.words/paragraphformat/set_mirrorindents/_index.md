---
title: Aspose::Words::ParagraphFormat::set_MirrorIndents method
linktitle: set_MirrorIndents
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::set_MirrorIndents method. Sets a flag indicating whether the left and right indents are of the same width in C++.'
type: docs
weight: 63500
url: /cpp/aspose.words/paragraphformat/set_mirrorindents/
---
## ParagraphFormat::set_MirrorIndents method


Sets a flag indicating whether the left and right indents are of the same width.

```cpp
void Aspose::Words::ParagraphFormat::set_MirrorIndents(bool value)
```

## Examples


Show how to make left and right indents the same.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Document.docx"));
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();

format->set_MirrorIndents(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.MirrorIndents.docx");
```
## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
