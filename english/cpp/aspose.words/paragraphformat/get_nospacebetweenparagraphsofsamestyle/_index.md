---
title: Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle method
linktitle: get_NoSpaceBetweenParagraphsOfSameStyle
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle method. When true, SpaceBefore and SpaceAfter will be ignored between the paragraphs of the same style in C++.'
type: docs
weight: 25000
url: /cpp/aspose.words/paragraphformat/get_nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle method


When **true**, [SpaceBefore](../get_spacebefore/) and [SpaceAfter](../get_spaceafter/) will be ignored between the paragraphs of the same style.

```cpp
bool Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle()
```

## Remarks


This setting only takes affect when applied to a paragraph style. If applied to a paragraph directly, it has no effect.

## Examples



Shows how to apply no spacing between paragraphs with the same style. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Apply a large amount of spacing before and after paragraphs that this builder will create.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Set the "NoSpaceBetweenParagraphsOfSameStyle" flag to "true" to apply
// no spacing between paragraphs with the same style, which will group similar paragraphs.
// Leave the "NoSpaceBetweenParagraphsOfSameStyle" flag as "false"
// to evenly apply spacing to every paragraph.
builder->get_ParagraphFormat()->set_NoSpaceBetweenParagraphsOfSameStyle(noSpaceBetweenParagraphsOfSameStyle);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Quote"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
