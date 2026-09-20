---
title: "Перечисление Aspose::Words::WatermarkType"
linktitle: "WatermarkType"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::WatermarkType. Указывает тип водяного знака в C++."
type: docs
weight: 131000
url: /ru/cpp/aspose.words/watermarktype/
---
## WatermarkType enum


Указывает тип водяного знака.

```cpp
enum class WatermarkType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Text | 0 | Указывает, что текст будет использоваться как водяной знак. Такой водяной знак соответствует объекту WordArt. |
| Image | 1 | Указывает, что изображение будет использоваться как водяной знак. Такой водяной знак соответствует фигуре с изображением. |
| None | 2 | Указывает, что водяной знак не установлен. |


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
