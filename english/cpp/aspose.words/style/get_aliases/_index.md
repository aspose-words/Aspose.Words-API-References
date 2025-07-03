---
title: Aspose::Words::Style::get_Aliases method
linktitle: get_Aliases
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Style::get_Aliases method. Gets all aliases of this style. If style has no aliases then empty array of string is returned in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/style/get_aliases/
---
## Style::get_Aliases method


Gets all aliases of this style. If style has no aliases then empty array of string is returned.

```cpp
System::ArrayPtr<System::String> Aspose::Words::Style::get_Aliases()
```


## Examples



Shows how to use style aliases. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Style with alias.docx");

// This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// If a style's name has multiple values separated by commas, each clause is a separate alias.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"MyStyle");
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"MyStyle Alias 1", u"MyStyle Alias 2"}), style->get_Aliases());
ASSERT_EQ(u"Title", style->get_BaseStyleName());
ASSERT_EQ(u"MyStyle Char", style->get_LinkedStyleName());

// We can reference a style using its alias, as well as its name.
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"MyStyle Alias 1"), doc->get_Styles()->idx_get(u"MyStyle Alias 2"));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 1"));
builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 2"));
builder->Write(u"Hello again!");

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_Style(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_ParagraphFormat()->get_Style());
```

## See Also

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
