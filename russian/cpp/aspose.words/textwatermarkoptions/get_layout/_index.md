---
title: "Aspose::Words::TextWatermarkOptions::get_Layout метод"
linktitle: "get_Layout"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TextWatermarkOptions::get_Layout метод. Получает или задает расположение водяного знака. Значение по умолчанию — Diagonal в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/textwatermarkoptions/get_layout/
---
## TextWatermarkOptions::get_Layout method


Получает или задает расположение водяного знака. Значение по умолчанию — [Diagonal](../../watermarklayout/).

```cpp
Aspose::Words::WatermarkLayout Aspose::Words::TextWatermarkOptions::get_Layout() const
```


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

* Enum [WatermarkLayout](../../watermarklayout/)
* Class [TextWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
