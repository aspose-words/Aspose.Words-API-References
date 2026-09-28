---
title: "Aspose::Words::Style::get_LinkedStyleName method"
linktitle: "get_LinkedStyleName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Style::get_LinkedStyleName. Получает/устанавливает имя стиля, связанного с этим. Возвращает пустую строку, если ни один стиль не связан в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words/style/get_linkedstylename/
---
## Style::get_LinkedStyleName method


Получает/устанавливает имя [Style](../), связанного с этим. Возвращает пустую строку, если ни один стиль не связан.

```cpp
System::String Aspose::Words::Style::get_LinkedStyleName()
```

## Примечания


Разрешено связывать только стиль абзаца со стилем символов и наоборот.

Установка LinkedStyleName для текущего стиля автоматически приводит к установке LinkedStyleName для связанного стиля.

Присвоение пустой строки эквивалентно разъединению ранее связанного стиля.

## Примеры



Показывает, как использовать псевдонимы стилей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Style with alias.docx");

// Этот документ содержит стиль с именем "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// Если у имени стиля несколько значений, разделённых запятыми, каждое значение является отдельным псевдонимом.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"MyStyle");
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"MyStyle Alias 1", u"MyStyle Alias 2"}), style->get_Aliases());
ASSERT_EQ(u"Title", style->get_BaseStyleName());
ASSERT_EQ(u"MyStyle Char", style->get_LinkedStyleName());

// Мы можем ссылаться на стиль, используя его псевдоним, а также его имя.
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"MyStyle Alias 1"), doc->get_Styles()->idx_get(u"MyStyle Alias 2"));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 1"));
builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 2"));
builder->Write(u"Hello again!");

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_Style(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_ParagraphFormat()->get_Style());
```


Показывает, как связывать стили между собой.
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

## См. также

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
