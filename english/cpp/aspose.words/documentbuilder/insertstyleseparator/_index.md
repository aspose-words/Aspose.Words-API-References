---
title: InsertStyleSeparator
second_title: Aspose.Words for C++ API Reference
description: Inserts style separator into the document.
type: docs
weight: 573
url: /cpp/aspose.words/documentbuilder/insertstyleseparator/
---
## DocumentBuilder.InsertStyleSeparator method


Inserts style separator into the document.

```cpp
void Aspose::Words::DocumentBuilder::InsertStyleSeparator()
```


## Examples




Shows how to work with style separators. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Each paragraph can only have one style.
// The InsertStyleSeparator method allows us to work around this limitation.
builder->get_ParagraphFormat()->set_StyleIdentifier(StyleIdentifier::Heading1);
builder->Write(u"This text is in a Heading style. ");
builder->InsertStyleSeparator();

SharedPtr<Style> paraStyle = builder->get_Document()->get_Styles()->Add(StyleType::Paragraph, u"MyParaStyle");
paraStyle->get_Font()->set_Bold(false);
paraStyle->get_Font()->set_Size(8);
paraStyle->get_Font()->set_Name(u"Arial");

builder->get_ParagraphFormat()->set_StyleName(paraStyle->get_Name());
builder->Write(u"This text is in a custom style. ");

// Calling the InsertStyleSeparator method creates another paragraph,
// which can have a different style to the previous. There will be no break between paragraphs.
// The text in the output document will look like one paragraph with two styles.
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());
ASSERT_EQ(u"Heading 1", doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_Style()->get_Name());
ASSERT_EQ(u"MyParaStyle", doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_ParagraphFormat()->get_Style()->get_Name());

doc->Save(ArtifactsDir + u"DocumentBuilder.InsertStyleSeparator.docx");
```

