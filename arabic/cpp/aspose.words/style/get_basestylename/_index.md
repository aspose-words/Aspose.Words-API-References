---
title: "طريقة Aspose::Words::Style::get_BaseStyleName"
linktitle: "get_BaseStyleName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Style::get_BaseStyleName. يحصل/يضبط اسم النمط الذي يُبنى عليه هذا النمط في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/style/get_basestylename/
---
## Style::get_BaseStyleName method


يحصل/يضبط اسم النمط الذي يُبنى عليه هذا النمط.

```cpp
System::String Aspose::Words::Style::get_BaseStyleName()
```


## أمثلة



يوضح كيفية استخدام أسماء المستعارة للنمط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Style with alias.docx");

// هذا المستند يحتوي على نمط مسمى "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// إذا كان اسم النمط يحتوي على قيم متعددة مفصولة بفواصل، فإن كل جزء يمثل اسمًا مستعارًا منفصلًا.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"MyStyle");
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"MyStyle Alias 1", u"MyStyle Alias 2"}), style->get_Aliases());
ASSERT_EQ(u"Title", style->get_BaseStyleName());
ASSERT_EQ(u"MyStyle Char", style->get_LinkedStyleName());

// يمكننا الإشارة إلى نمط باستخدام اسمه المستعار، وكذلك اسمه الأصلي.
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"MyStyle Alias 1"), doc->get_Styles()->idx_get(u"MyStyle Alias 2"));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 1"));
builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 2"));
builder->Write(u"Hello again!");

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_Style(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_ParagraphFormat()->get_Style());
```

## انظر أيضًا

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
