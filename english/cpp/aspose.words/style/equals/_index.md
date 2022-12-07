---
title: Equals
second_title: Aspose.Words for C++ API Reference
description: Compares with the specified style. Styles Istds are compared for built-in styles only. Styles defaults are not included in comparison. Base style, linked style and next paragraph style are recursively compared.
type: docs
weight: 14
url: /cpp/aspose.words/style/equals/
---
## Style::Equals method


Compares with the specified style. Styles Istds are compared for built-in styles only. Styles defaults are not included in comparison. Base style, linked style and next paragraph style are recursively compared.

```cpp
bool Aspose::Words::Style::Equals(const System::SharedPtr<Aspose::Words::Style> &style)
```


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
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
