---
title: "Класс Aspose::Words::Saving::PageSet"
linktitle: "PageSet"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Saving::PageSet. Описывает произвольный набор страниц. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 20000
url: /ru/cpp/aspose.words.saving/pageset/
---
## PageSet class


Описывает случайный набор страниц. Чтобы узнать больше, посетите статью документации [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class PageSet : public System::Collections::Generic::IEnumerable<int32_t>
```

## Методы

| Метод | Описание |
| --- | --- |
| static [get_All](./get_all/)() | Возвращает набор со всеми страницами документа в их исходном порядке. |
| static [get_Even](./get_even/)() | Возвращает набор со всеми четными страницами документа в их исходном порядке. |
| static [get_Odd](./get_odd/)() | Возвращает набор со всеми нечетными страницами документа в их исходном порядке. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PageSet](./pageset/)(int32_t) | Создаёт набор из одной страницы на основе точного индекса страницы. |
| [PageSet](./pageset/)(const System::ArrayPtr\<int32_t\>\&) | Создаёт набор страниц на основе точных индексов страниц. |
| [PageSet](./pageset/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Saving::PageRange\>\>\&) | Создаёт набор страниц на основе диапазонов. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как отобразить одну страницу документа в изображение JPEG.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Создайте объект "ImageSaveOptions", который мы можем передать методу "Save" документа
// чтобы изменить способ, которым этот метод отображает документ в изображение.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Установите "PageSet" в "1", чтобы выбрать вторую страницу через
// ноль‑базовый индекс, с которого начинать отображение документа.
options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(1));

// Когда мы сохраняем документ в формате JPEG, Aspose.Words отображает только одну страницу.
// Это изображение будет содержать одну страницу, начиная со второй страницы,
// которая будет просто второй страницей оригинального документа.
doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.OnePage.jpg", options);
```

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
