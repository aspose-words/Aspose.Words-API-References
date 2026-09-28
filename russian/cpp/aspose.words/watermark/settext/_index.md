---
title: "Метод Aspose::Words::Watermark::SetText"
linktitle: "SetText"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Watermark::SetText. Добавляет текстовый водяной знак в документ в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words/watermark/settext/
---
## Watermark::SetText(const System::String\&) method


Добавляет текстовый водяной знак в документ.

```cpp
void Aspose::Words::Watermark::SetText(const System::String &text)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| текст | const System::String\& | Текст, отображаемый в виде водяного знака. |

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

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetText(const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) method


Добавляет текстовый водяной знак в документ.

```cpp
void Aspose::Words::Watermark::SetText(const System::String &text, const System::SharedPtr<Aspose::Words::TextWatermarkOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| текст | const System::String\& | Текст, отображаемый в виде водяного знака. |
| параметры | const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\& | Определяет дополнительные параметры для текстового водяного знака. |

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

* Class [TextWatermarkOptions](../../textwatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
