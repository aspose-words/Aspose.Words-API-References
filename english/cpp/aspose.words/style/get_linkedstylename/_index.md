---
title: Aspose::Words::Style::get_LinkedStyleName method
linktitle: get_LinkedStyleName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Style::get_LinkedStyleName method. Gets/sets the name of the Style linked to this one. Returns empty string if no styles are linked in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words/style/get_linkedstylename/
---
## Style::get_LinkedStyleName method


Gets/sets the name of the [Style](../) linked to this one. Returns empty string if no styles are linked.

```cpp
System::String Aspose::Words::Style::get_LinkedStyleName()
```

## Remarks


It is only allowed to link the paragraph style to the character style and vice versa.

Setting LinkedStyleName for the current style automatically leads to setting LinkedStyleName for the linked style.

Assigning the empty string is equivalent to unlinking the previously linked style.

## Examples



Shows how to use style aliases. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Style with alias.docx");

// This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// If a style's name has multiple values separated by commas, each clause is a separate alias.
SharedPtr<Style> style = doc->get_Styles()->idx_get(u"MyStyle");
ASPOSE_ASSERT_EQ(MakeArray<String>({u"MyStyle Alias 1", u"MyStyle Alias 2"}), style->get_Aliases());
ASSERT_EQ(u"Title", style->get_BaseStyleName());
ASSERT_EQ(u"MyStyle Char", style->get_LinkedStyleName());

// We can reference a style using its alias, as well as its name.
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"MyStyle Alias 1"), doc->get_Styles()->idx_get(u"MyStyle Alias 2"));

auto builder = MakeObject<DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 1"));
builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 2"));
builder->Write(u"Hello again!");

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_Style(),
                 doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_ParagraphFormat()->get_Style());
```

## See Also

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
