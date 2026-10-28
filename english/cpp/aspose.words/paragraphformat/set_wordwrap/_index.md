---
title: Aspose::Words::ParagraphFormat::set_WordWrap method
linktitle: set_WordWrap
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::set_WordWrap method. If this property is false, Latin text in the middle of a word can be wrapped for the current paragraph. Otherwise Latin text is wrapped by whole words in C++.'
type: docs
weight: 79000
url: /cpp/aspose.words/paragraphformat/set_wordwrap/
---
## ParagraphFormat::set_WordWrap method


If this property is **false**, Latin text in the middle of a word can be wrapped for the current paragraph. Otherwise Latin text is wrapped by whole words.

```cpp
void Aspose::Words::ParagraphFormat::set_WordWrap(bool value)
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
