---
title: "Aspose::Words::Style::get_AutomaticallyUpdate метод"
linktitle: "get_AutomaticallyUpdate"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Style::get_AutomaticallyUpdate метод. Указывает, автоматически ли переопределяется этот стиль на основе соответствующего значения в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/style/get_automaticallyupdate/
---
## Style::get_AutomaticallyUpdate method


Указывает, переопределяется ли этот стиль автоматически на основе соответствующего значения.

```cpp
bool Aspose::Words::Style::get_AutomaticallyUpdate() const
```

## Примечания


Если значение свойства установлено в true, MS Word автоматически переопределяет текущий стиль, когда соответствующее форматирование абзаца изменено.

Свойство AutomaticallyUpdate применимо только к стилям абзацев.

Значение по умолчанию — **false**.

## Примеры



Показывает, как создать и применить пользовательский стиль.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// Автоматически переопределить стиль.
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Примените один из стилей документа к абзацу, который создает DocumentBuilder.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// Удалите наш пользовательский стиль из коллекции стилей документа.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// Любой текст, использующий удалённый стиль, возвращается к форматированию по умолчанию.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```

## См. также

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
