---
title: "Aspose::Words::Saving::MultiPageLayout class"
linktitle: "MultiPageLayout"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::MultiPageLayout class. Определяет макет для рендеринга нескольких страниц в один вывод в C++."
type: docs
weight: 14500
url: /ru/cpp/aspose.words.saving/multipagelayout/
---
## MultiPageLayout class


Определяет макет для рендеринга нескольких страниц в один вывод.

```cpp
class MultiPageLayout : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Получает цвет фона вывода. По умолчанию **Empty**. |
| [get_BorderColor](./get_bordercolor/)() | Получает цвет границы страниц. По умолчанию **Empty**. |
| [get_BorderWidth](./get_borderwidth/)() const | Получает ширину границы страниц. По умолчанию 0. |
| [GetType](./gettype/)() const override |  |
| static [Grid](./grid/)(int32_t, float, float) | Создаёт макет, в котором страницы рендерятся слева направо, сверху вниз, в сетке с указанным числом столбцов. |
| static [Horizontal](./horizontal/)(float) | Создаёт макет, в котором все указанные страницы рендерятся горизонтально рядом, слева направо, в едином выводе. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Устанавливает цвет фона вывода. По умолчанию **Empty**. |
| [set_BorderColor](./set_bordercolor/)(System::Drawing::Color) | Устанавливает цвет границы страниц. По умолчанию **Empty**. |
| [set_BorderWidth](./set_borderwidth/)(float) | Устанавливает ширину границы страниц. По умолчанию 0. |
| static [SinglePage](./singlepage/)() | Создаёт макет, который рендерит только первую из указанных страниц. |
| static [TiffFrames](./tiffframes/)() | Создаёт макет, где каждая страница рендерится как отдельный кадр в многокадровом TIFF‑изображении. Применимо только к форматам изображений TIFF. |
| static [Type](./type/)() |  |
| static [Vertical](./vertical/)(float) | Создает макет, в котором все указанные страницы отображаются вертикально одна под другой в едином выводе. |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
