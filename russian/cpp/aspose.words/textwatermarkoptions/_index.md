---
title: "Aspose::Words::TextWatermarkOptions class"
linktitle: "TextWatermarkOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::TextWatermarkOptions. Содержит параметры, которые можно указать при добавлении текстового водяного знака. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 72000
url: /ru/cpp/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class


Содержит параметры, которые можно указать при добавлении водяного знака с текстом. Чтобы узнать больше, посетите статью документации [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class TextWatermarkOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Color](./get_color/)() const | Получает или задаёт цвет шрифта. Значение по умолчанию — **Silver**. |
| [get_FontFamily](./get_fontfamily/)() const | Получает или задаёт название семейства шрифтов. Значение по умолчанию — "Calibri". |
| [get_FontSize](./get_fontsize/)() const | Получает или задаёт размер шрифта. Значение по умолчанию — 0 — авто. |
| [get_IsSemitrasparent](./get_issemitrasparent/)() const | Получает или задаёт логическое значение, отвечающее за непрозрачность водяного знака. Значение по умолчанию — **true**. |
| [get_Layout](./get_layout/)() const | Получает или задаёт расположение водяного знака. Значение по умолчанию — [Diagonal](../watermarklayout/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | Сеттер для [Aspose::Words::TextWatermarkOptions::get_Color](./get_color/). |
| [set_FontFamily](./set_fontfamily/)(const System::String\&) | Сеттер для [Aspose::Words::TextWatermarkOptions::get_FontFamily](./get_fontfamily/). |
| [set_FontSize](./set_fontsize/)(float) | Сеттер для [Aspose::Words::TextWatermarkOptions::get_FontSize](./get_fontsize/). |
| [set_IsSemitrasparent](./set_issemitrasparent/)(bool) | Сеттер для [Aspose::Words::TextWatermarkOptions::get_IsSemitrasparent](./get_issemitrasparent/). |
| [set_Layout](./set_layout/)(Aspose::Words::WatermarkLayout) | Сеттер для [Aspose::Words::TextWatermarkOptions::get_Layout](./get_layout/). |
| [TextWatermarkOptions](./textwatermarkoptions/)() |  |
| static [Type](./type/)() |  |

## Примеры



Показывает, как создать текстовый водяной знак.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Добавьте простой текстовый водяной знак.
doc->get_Watermark()->SetText(u"Aspose Watermark");

// Если мы хотим изменить форматирование текста, используя его в качестве водяного знака,
// мы можем сделать это, передав объект TextWatermarkOptions при создании водяного знака.
auto textWatermarkOptions = System::MakeObject<Aspose::Words::TextWatermarkOptions>();
textWatermarkOptions->set_FontFamily(u"Arial");
textWatermarkOptions->set_FontSize(36.0f);
textWatermarkOptions->set_Color(System::Drawing::Color::get_Black());
textWatermarkOptions->set_Layout(Aspose::Words::WatermarkLayout::Diagonal);
textWatermarkOptions->set_IsSemitrasparent(false);

doc->get_Watermark()->SetText(u"Aspose Watermark", textWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.TextWatermark.docx");

// Мы можем удалить водяной знак из документа, как показано здесь.
if (doc->get_Watermark()->get_Type() == Aspose::Words::WatermarkType::Text)
{
    doc->get_Watermark()->Remove();
}
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
