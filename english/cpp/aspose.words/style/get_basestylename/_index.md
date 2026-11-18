---
title: Aspose::Words::Style::get_BaseStyleName method
linktitle: get_BaseStyleName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Style::get_BaseStyleName method. Gets/sets the name of the style this style is based on in C++.'
type: docs
weight: 22138
url: /cpp/aspose.words/style/get_basestylename/
---
## Style::get_BaseStyleName method


Gets/sets the name of the style this style is based on.

```cpp
System::String Aspose::Words::Style::get_BaseStyleName()
```

## Remarks

 This will be an empty string if the style is not based on any other style and it can be set to an empty string. 
## Examples


Shows how to use style aliases.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Style with alias.docx"));

// This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// If a style's name has multiple values separated by commas, each clause is a separate alias.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"MyStyle");
ASPOSE_ASSERT_EQ(style->get_Aliases(), System::MakeArray<System::String>({u"MyStyle Alias 1", u"MyStyle Alias 2"}));
ASSERT_EQ(style->get_BaseStyleName(), u"Title");
ASSERT_EQ(style->get_LinkedStyleName(), u"MyStyle Char");

// We can reference a style using its alias, as well as its name.
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"MyStyle Alias 2"), doc->get_Styles()->idx_get(u"MyStyle Alias 1"));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 1"));
builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 2"));
builder->Write(u"Hello again!");

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_ParagraphFormat()->get_Style(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_Style());
```
## See Also

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
