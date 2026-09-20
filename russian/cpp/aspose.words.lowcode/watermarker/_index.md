---
title: "Aspose::Words::LowCode::Watermarker class"
linktitle: "Watermarker"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::LowCode::Watermarker. Предоставляет методы, предназначенные для вставки водяных знаков в документы на C++."
type: docs
weight: 1750
url: /ru/cpp/aspose.words.lowcode/watermarker/
---
## Watermarker class


Предоставляет методы, предназначенные для вставки водяных знаков в документы.

```cpp
class Watermarker : public Aspose::Words::LowCode::Processor
```

## Методы

| Метод | Описание |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::WatermarkerContext\>\&) | Создает новый экземпляр процессора водяных знаков. |
| [Execute](../processor/execute/)() | Выполнить действие процессора. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Выполнить действие процессора, позволяя отменить задачу обработки документа с использованием указанного токена отмены. |
| [From](../processor/from/)(const System::String\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Указывает входной документ для обработки. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::String\&) | Добавляет изображение водяного знака в документ. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Добавляет изображение водяного знака в документ с параметрами. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) | Добавляет изображение водяного знака в документ с параметрами и указанным форматом сохранения. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Добавляет изображение водяного знака в документ с параметрами и указанным форматом сохранения. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | Добавляет изображение водяного знака в документ с параметрами и указанным форматом сохранения. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Добавляет изображение водяного знака в документ с параметрами и указанным форматом сохранения. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&) | Добавляет изображение водяного знака в документ из потоков с параметрами. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Добавляет изображение водяного знака в документ из потоков с параметрами. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&) | Добавляет изображение водяного знака в документ из потоков с параметрами. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Добавляет изображение водяного знака в документ из потоков с параметрами. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&) | Добавляет изображение водяного знака в документ из потоков с параметрами. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Добавляет изображение водяного знака в документ из потоков с параметрами. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Добавляет изображение водяного знака в документ из потоков с параметрами. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Добавляет изображение водяного знака в документ из потоков с параметрами. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::String\&) | Добавляет текстовый водяной знак в документ. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Добавляет текстовый водяной знак в документ с параметрами. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) | Добавляет текстовый водяной знак в документ с параметрами и указанным форматом сохранения. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Добавляет текстовый водяной знак в документ с параметрами и указанным форматом сохранения. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | Добавляет текстовый водяной знак в документ с параметрами и указанным форматом сохранения. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Добавляет текстовый водяной знак в документ с параметрами и указанным форматом сохранения. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&) | Добавляет текстовый водяной знак в документ из потоков с параметрами. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Добавляет текстовый водяной знак в документ из потоков с параметрами. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | Добавляет текстовый водяной знак в документ из потоков с параметрами. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Добавляет текстовый водяной знак в документ из потоков с параметрами. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&) | Добавляет текстовый водяной знак в документ с параметрами. Рендерит вывод в изображения. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Добавляет текстовый водяной знак в документ с параметрами. Рендерит вывод в изображения. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&) | Добавляет текстовый водяной знак в документ с параметрами. Рендерит вывод в изображения. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Добавляет текстовый водяной знак в документ с параметрами. Рендерит вывод в изображения. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&) | Добавляет изображение водяного знака в документ с параметрами. Рендерит вывод в изображения. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Добавляет изображение водяного знака в документ с параметрами. Рендерит вывод в изображения. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Добавляет изображение водяного знака в документ с параметрами. Рендерит вывод в изображения. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Добавляет изображение водяного знака в документ с параметрами. Рендерит вывод в изображения. |
| [To](../processor/to/)(const System::String\&) | Указывает выходной файл для процессора. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Указывает выходной файл для процессора. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Указывает выходной файл для процессора. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Указывает выходной поток для процессора. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Указывает выходной поток для процессора. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## См. также

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
