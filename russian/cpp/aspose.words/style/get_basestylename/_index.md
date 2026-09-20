---
title: "Aspose::Words::Style::get_BaseStyleName method"
linktitle: "get_BaseStyleName"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Style::get_BaseStyleName method. Получает/устанавливает имя стиля, на котором основан данный стиль, в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/style/get_basestylename/
---
## Style::get_BaseStyleName method


Получает/устанавливает имя стиля, на котором основан этот стиль.

```cpp
System::String Aspose::Words::Style::get_BaseStyleName()
```


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

## См. также

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
