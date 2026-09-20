---
title: "Aspose::Words::DocumentBuilder::PopFont метод"
linktitle: "PopFont"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::PopFont метод. Получает форматирование символов, ранее сохранённое в стеке, в C++."
type: docs
weight: 62000
url: /ru/cpp/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder::PopFont method


Получает форматирование символов, ранее сохранённое в стеке.

```cpp
void Aspose::Words::DocumentBuilder::PopFont()
```


## Примеры



Показывает, как использовать стек форматирования построителя документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Настройте форматирование шрифта, затем запишите текст, который будет перед гиперссылкой.
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Size(24);
builder->Write(u"To visit Google, hold Ctrl and click ");

// Сохраните текущую конфигурацию форматирования в стеке.
builder->PushFont();

// Измените текущее форматирование построителя, применив новый стиль.
builder->get_Font()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Hyperlink);
builder->InsertHyperlink(u"here", u"http://www.google.com", false);

ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::Single, builder->get_Font()->get_Underline());

// Восстановите сохранённое ранее форматирование шрифта и удалите элемент из стека.
builder->PopFont();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), builder->get_Font()->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Underline::None, builder->get_Font()->get_Underline());

builder->Write(u". We hope you enjoyed the example.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.PushPopFont.docx");
```

## См. также

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
