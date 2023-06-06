---
title: Aspose::Words::Font::get_StrikeThrough method
linktitle: get_StrikeThrough
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_StrikeThrough method. True if the font is formatted as strikethrough text in C++.'
type: docs
weight: 41000
url: /cpp/aspose.words/font/get_strikethrough/
---
## Font::get_StrikeThrough method


True if the font is formatted as strikethrough text.

```cpp
bool Aspose::Words::Font::get_StrikeThrough()
```


## Examples



Shows how to add a line strikethrough to text. 
```cpp
auto doc = MakeObject<Document>();
auto para = System::ExplicitCast<Paragraph>(doc->GetChild(NodeType::Paragraph, 0, true));

auto run = MakeObject<Run>(doc, u"Text with a single-line strikethrough.");
run->get_Font()->set_StrikeThrough(true);
para->AppendChild(run);

para = System::ExplicitCast<Paragraph>(para->get_ParentNode()->AppendChild(MakeObject<Paragraph>(doc)));

run = MakeObject<Run>(doc, u"Text with a double-line strikethrough.");
run->get_Font()->set_DoubleStrikeThrough(true);
para->AppendChild(run);

doc->Save(ArtifactsDir + u"Font.StrikeThrough.docx");
```

## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
