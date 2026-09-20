---
title: "Класс Aspose::Words::Watermark"
linktitle: "Водяной знак"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Watermark. Представляет класс для работы с водяным знаком документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 76000
url: /ru/cpp/aspose.words/watermark/
---
## Watermark class


Представляет класс для работы с водяным знаком документа. Чтобы узнать больше, посетите статью документации [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/).

```cpp
class Watermark : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Type](./get_type/)() | Получает тип водяного знака. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Удаляет водяной знак. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Добавляет изображение водяного знака в документ. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Добавляет изображение водяного знака в документ. |
| [SetImage](./setimage/)(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Добавляет изображение водяного знака в документ. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Добавляет изображение водяного знака в документ. |
| [SetText](./settext/)(const System::String\&) | Добавляет текстовый водяной знак в документ. |
| [SetText](./settext/)(const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Добавляет текстовый водяной знак в документ. |
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
