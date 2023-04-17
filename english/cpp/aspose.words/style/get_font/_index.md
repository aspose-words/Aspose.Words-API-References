---
title: Aspose::Words::Style::get_Font method
linktitle: get_Font
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Style::get_Font method. Gets the character formatting of the style in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words/style/get_font/
---
## Style::get_Font method


Gets the character formatting of the style.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Style::get_Font()
```

## Remarks


For list styles this property returns **null**.

## Examples



Shows how to create and apply a custom style. 
```cpp
auto doc = MakeObject<Document>();

SharedPtr<Style> style = doc->get_Styles()->Add(StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());

auto builder = MakeObject<DocumentBuilder>(doc);

// Apply one of the styles from the document to the paragraph that the document builder is creating.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

SharedPtr<Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// Remove our custom style from the document's styles collection.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// Any text that used a removed style reverts to the default formatting.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any([](SharedPtr<Style> s) { return s->get_Name() == u"MyStyle"; }));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```


Shows how to create and use a paragraph style with list formatting. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Create a custom paragraph style.
SharedPtr<Style> style = doc->get_Styles()->Add(StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Create a list and make sure the paragraphs that use this style will use this list.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Apply the paragraph style to the document builder's current paragraph, and then add some text.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Change the document builder's style to one that has no list formatting and write another paragraph.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(ArtifactsDir + u"Styles.ParagraphStyleBulletedList.docx");
```

## See Also

* Class [Font](../../font/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
