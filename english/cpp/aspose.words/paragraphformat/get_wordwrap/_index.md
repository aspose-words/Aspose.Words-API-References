---
title: Aspose::Words::ParagraphFormat::get_WordWrap method
linktitle: get_WordWrap
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::get_WordWrap method. If this property is false, Latin text in the middle of a word can be wrapped for the current paragraph. Otherwise Latin text is wrapped by whole words in C++.'
type: docs
weight: 42000
url: /cpp/aspose.words/paragraphformat/get_wordwrap/
---
## ParagraphFormat::get_WordWrap method


If this property is **false**, Latin text in the middle of a word can be wrapped for the current paragraph. Otherwise Latin text is wrapped by whole words.

```cpp
bool Aspose::Words::ParagraphFormat::get_WordWrap()
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
* Library [Aspose.Words for C++](../../../)
