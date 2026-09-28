---
title: "Метод Aspose::Words::Saving::ImageSaveOptions::get_PageLayout"
linktitle: "get_PageLayout"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::ImageSaveOptions::get_PageLayout. Получает или задает макет, используемый при рендеринге нескольких страниц в один вывод в C++."
type: docs
weight: 9500
url: /ru/cpp/aspose.words.saving/imagesaveoptions/get_pagelayout/
---
## ImageSaveOptions::get_PageLayout method


Получает или задаёт макет, используемый при рендеринге нескольких страниц в один вывод.

```cpp
System::SharedPtr<Aspose::Words::Saving::MultiPageLayout> Aspose::Words::Saving::ImageSaveOptions::get_PageLayout() const
```

## Примечания


Используйте один из фабричных методов [MultiPageLayout](../../multipagelayout/), чтобы настроить это свойство.

Для [Tiff](../../../aspose.words/saveformat/) значение по умолчанию — [TiffFrames](../../multipagelayout/tiffframes/). Для других форматов значение по умолчанию — [SinglePage](../../multipagelayout/singlepage/).

Это свойство действует только при сохранении в следующих форматах: [Jpeg](../../../aspose.words/saveformat/), [Gif](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Tiff](../../../aspose.words/saveformat/), [WebP](../).

## Примеры



Показывает, как сохранить документ в изображение JPG с настройками многостраничного макета.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Настройте сеточный макет с:
// - 3 столбца в строке.
// - 10 пунктов интервала между страницами (по горизонтали и вертикали).
options->set_PageLayout(Aspose::Words::Saving::MultiPageLayout::Grid(3, 10.0f, 10.0f));

// Альтернативные макеты:
// options.PageLayout = MultiPageLayout.Horizontal(10);
// options.PageLayout = MultiPageLayout.Vertical(10);

// Настройте фон и границу.
options->get_PageLayout()->set_BackColor(System::Drawing::Color::get_LightGray());
options->get_PageLayout()->set_BorderColor(System::Drawing::Color::get_Blue());
options->get_PageLayout()->set_BorderWidth(2.0f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.GridLayout.jpg", options);
```

## См. также

* Class [MultiPageLayout](../../multipagelayout/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
