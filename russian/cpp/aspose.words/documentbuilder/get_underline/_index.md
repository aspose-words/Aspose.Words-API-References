---
title: "Метод Aspose::Words::DocumentBuilder::get_Underline"
linktitle: "get_Underline"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBuilder::get_Underline. Получает/устанавливает тип подчеркивания для текущего шрифта в C++."
type: docs
weight: 26000
url: /ru/cpp/aspose.words/documentbuilder/get_underline/
---
## DocumentBuilder::get_Underline method


Получает/устанавливает тип подчеркивания для текущего шрифта.

```cpp
Aspose::Words::Underline Aspose::Words::DocumentBuilder::get_Underline()
```


## Примеры



Показывает, как форматировать текст, вставленный построителем документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Dash);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(32);

// Построитель применяет форматирование к текущему абзацу и к любому новому тексту, добавленному им позже.
builder->Writeln(u"Large, blue, and underlined text.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertUnderline.docx");
```

## См. также

* Enum [Underline](../../underline/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
