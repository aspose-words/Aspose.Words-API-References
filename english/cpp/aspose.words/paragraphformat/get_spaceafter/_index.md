---
title: Aspose::Words::ParagraphFormat::get_SpaceAfter method
linktitle: get_SpaceAfter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::get_SpaceAfter method. Gets or sets the amount of spacing (in points) after the paragraph in C++.'
type: docs
weight: 31000
url: /cpp/aspose.words/paragraphformat/get_spaceafter/
---
## ParagraphFormat::get_SpaceAfter method


Gets or sets the amount of spacing (in points) after the paragraph.

```cpp
double Aspose::Words::ParagraphFormat::get_SpaceAfter()
```

## Remarks


Has no effect when [SpaceAfterAuto](../get_spaceafterauto/) is **true**.

Valid values ​​range from 0 to 1584 inclusive.

## Examples



Shows how to set automatic paragraph spacing. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Apply a large amount of spacing before and after paragraphs that this builder will create.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Set these flags to "true" to apply automatic spacing,
// effectively ignoring the spacing in the properties we set above.
// Leave them as "false" will apply our custom paragraph spacing.
builder->get_ParagraphFormat()->set_SpaceAfterAuto(autoSpacing);
builder->get_ParagraphFormat()->set_SpaceBeforeAuto(autoSpacing);

// Insert two paragraphs that will have spacing above and below them and save the document.
builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingAuto.docx");
```


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
