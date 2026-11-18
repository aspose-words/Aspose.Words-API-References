---
title: Aspose::Words::ParagraphFormat::set_BaselineAlignment method
linktitle: set_BaselineAlignment
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::set_BaselineAlignment method. Sets fonts vertical position on a line in C++.'
type: docs
weight: 47500
url: /cpp/aspose.words/paragraphformat/set_baselinealignment/
---
## ParagraphFormat::set_BaselineAlignment method


Sets fonts vertical position on a line.

```cpp
void Aspose::Words::ParagraphFormat::set_BaselineAlignment(Aspose::Words::BaselineAlignment value)
```

## Examples


Shows how to set fonts vertical position on a line.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Office math.docx"));

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();
if (format->get_BaselineAlignment() == BaselineAlignment::Auto)
{
    format->set_BaselineAlignment(BaselineAlignment::Top);
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphBaselineAlignment.docx");
```
## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
