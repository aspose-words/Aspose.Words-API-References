---
title: Remove
second_title: Aspose.Words for C++ API Reference
description: Removes the specified style from the document.
type: docs
weight: 222
url: /cpp/aspose.words/style/remove/
---
## Style::Remove method


Removes the specified style from the document.

```cpp
void Aspose::Words::Style::Remove()
```

## Remarks


[Style](../) removal has following effects on the document model:

* All references to the style are removed from corresponding paragraphs, runs and tables.
* If base style is removed its formatting is moved to child styles.
* If style to be deleted has a linked style, then both of these are deleted.



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

## See Also

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
