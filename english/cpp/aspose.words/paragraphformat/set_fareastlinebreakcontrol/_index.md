---
title: Aspose::Words::ParagraphFormat::set_FarEastLineBreakControl method
linktitle: set_FarEastLineBreakControl
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::set_FarEastLineBreakControl method. Sets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph in C++.'
type: docs
weight: 53000
url: /cpp/aspose.words/paragraphformat/set_fareastlinebreakcontrol/
---
## ParagraphFormat::set_FarEastLineBreakControl method


Sets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph.

```cpp
void Aspose::Words::ParagraphFormat::set_FarEastLineBreakControl(bool value)
```

## Examples


Shows how to set special properties for Asian typography.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Document.docx"));

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_FarEastLineBreakControl(true);
format->set_WordWrap(false);
format->set_HangingPunctuation(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.AsianTypographyProperties.docx");
```
## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
