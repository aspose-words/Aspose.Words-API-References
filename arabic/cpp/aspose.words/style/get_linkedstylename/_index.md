---
title: "طريقة Aspose::Words::Style::get_LinkedStyleName"
linktitle: "get_LinkedStyleName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Style::get_LinkedStyleName. يحصل/يضبط اسم النمط المرتبط بهذا النمط. يرجع سلسلة فارغة إذا لم يتم ربط أي أنماط في C++."
type: docs
weight: 11000
url: /ar/cpp/aspose.words/style/get_linkedstylename/
---
## Style::get_LinkedStyleName method


يحصل/يضبط اسم الـ [Style](../) المرتبط بهذا النمط. يرجع سلسلة فارغة إذا لم يتم ربط أي أنماط.

```cpp
System::String Aspose::Words::Style::get_LinkedStyleName()
```

## ملاحظات


يسمح فقط بربط نمط الفقرة بنمط الحرف والعكس بالعكس.

ضبط LinkedStyleName للنمط الحالي يؤدي تلقائيًا إلى ضبط LinkedStyleName للنمط المرتبط.

تعيين السلسلة الفارغة يعادل إلغاء ربط النمط المرتبط مسبقًا.

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


يوضح كيفية ربط الأنماط ببعضها البعض.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1);

System::SharedPtr<Aspose::Words::Style> styleHeading1Char = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"Heading 1 Char");
styleHeading1Char->get_Font()->set_Name(u"Verdana");
styleHeading1Char->get_Font()->set_Bold(true);
styleHeading1Char->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::Dot);
styleHeading1Char->get_Font()->get_Border()->set_LineWidth(15);

styleHeading1->set_LinkedStyleName(u"Heading 1 Char");

ASSERT_EQ(u"Heading 1 Char", styleHeading1->get_LinkedStyleName());
ASSERT_EQ(u"Heading 1", styleHeading1Char->get_LinkedStyleName());
```

## انظر أيضًا

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
