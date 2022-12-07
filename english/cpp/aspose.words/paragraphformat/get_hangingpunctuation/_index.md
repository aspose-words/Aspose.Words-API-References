---
title: get_HangingPunctuation
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a flag indicating whether hanging punctuation is enabled for the current paragraph.
type: docs
weight: 170
url: /cpp/aspose.words/paragraphformat/get_hangingpunctuation/
---
## ParagraphFormat::get_HangingPunctuation method


Gets or sets a flag indicating whether hanging punctuation is enabled for the current paragraph.

```cpp
bool Aspose::Words::ParagraphFormat::get_HangingPunctuation()
```


## Examples



Shows how to set special properties for Asian typography. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

SharedPtr<ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_FarEastLineBreakControl(true);
format->set_WordWrap(false);
format->set_HangingPunctuation(true);

doc->Save(ArtifactsDir + u"ParagraphFormat.AsianTypographyProperties.docx");
```

## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
