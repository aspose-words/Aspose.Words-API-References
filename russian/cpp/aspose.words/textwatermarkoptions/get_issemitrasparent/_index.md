---
title: "Метод Aspose::Words::TextWatermarkOptions::get_IsSemitrasparent"
linktitle: "get_IsSemitrasparent"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::TextWatermarkOptions::get_IsSemitrasparent. Получает или задает логическое значение, отвечающее за непрозрачность водяного знака. Значение по умолчанию — true в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/textwatermarkoptions/get_issemitrasparent/
---
## TextWatermarkOptions::get_IsSemitrasparent method


Получает или задаёт логическое значение, отвечающее за непрозрачность водяного знака. Значение по умолчанию — **true**.

```cpp
bool Aspose::Words::TextWatermarkOptions::get_IsSemitrasparent() const
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

* Class [TextWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
