---
title: "Aspose::Words::WatermarkLayout enum"
linktitle: "WatermarkLayout"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::WatermarkLayout enum. Определяет расположение водяного знака относительно его центра в C++."
type: docs
weight: 130000
url: /ru/cpp/aspose.words/watermarklayout/
---
## WatermarkLayout enum


Определяет расположение водяного знака относительно его центра.

```cpp
enum class WatermarkLayout
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Горизонтальная | 0 | Горизонтальное расположение водяного знака. Соответствует вращению на 0 градусов. |
| Diagonal | 315 | Диагональное расположение водяного знака. Соответствует вращению на 315 градусов. |


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
