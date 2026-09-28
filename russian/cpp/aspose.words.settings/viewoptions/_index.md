---
title: "Aspose::Words::Settings::ViewOptions класс"
linktitle: "ViewOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::ViewOptions class. Предоставляет различные параметры, которые управляют тем, как документ отображается в Microsoft Word. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.settings/viewoptions/
---
## ViewOptions class


Предоставляет различные параметры, которые контролируют отображение документа в Microsoft Word. Чтобы узнать больше, посетите статью документации [Work with Options and Appearance of Word Documents](https://docs.aspose.com/words/cpp/work-with-word-document-options-and-appearance/).

```cpp
class ViewOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_DisplayBackgroundShape](./get_displaybackgroundshape/)() const | Управляет отображением фоновой фигуры в режиме разметки печати. |
| [get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/)() const | Отключает отображение пространства между верхом текста и верхним краем страницы. |
| [get_FormsDesign](./get_formsdesign/)() const | Указывает, находится ли документ в режиме разработки форм. |
| [get_ViewType](./get_viewtype/)() const | Управляет режимом просмотра в Microsoft Word. |
| [get_ZoomPercent](./get_zoompercent/)() const | Получает или задает процент, с которым вы хотите просматривать документ. |
| [get_ZoomType](./get_zoomtype/)() const | Получает или задает значение масштабирования, основанное на размере окна. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DisplayBackgroundShape](./set_displaybackgroundshape/)(bool) | Сеттер для [Aspose::Words::Settings::ViewOptions::get_DisplayBackgroundShape](./get_displaybackgroundshape/). |
| [set_DoNotDisplayPageBoundaries](./set_donotdisplaypageboundaries/)(bool) | Сеттер для [Aspose::Words::Settings::ViewOptions::get_DoNotDisplayPageBoundaries](./get_donotdisplaypageboundaries/). |
| [set_FormsDesign](./set_formsdesign/)(bool) | Сеттер для [Aspose::Words::Settings::ViewOptions::get_FormsDesign](./get_formsdesign/). |
| [set_ViewType](./set_viewtype/)(Aspose::Words::Settings::ViewType) | Сеттер для [Aspose::Words::Settings::ViewOptions::get_ViewType](./get_viewtype/). |
| [set_ZoomPercent](./set_zoompercent/)(int32_t) | Сеттер для [Aspose::Words::Settings::ViewOptions::get_ZoomPercent](./get_zoompercent/). |
| [set_ZoomType](./set_zoomtype/)(Aspose::Words::Settings::ZoomType) | Сеттер для [Aspose::Words::Settings::ViewOptions::get_ZoomType](./get_zoomtype/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как задать пользовательский коэффициент масштабирования, который более старые версии Microsoft Word применяют к документу при загрузке.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(Aspose::Words::Settings::ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(Aspose::Words::Settings::ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(Aspose::Words::Settings::ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomPercentage.doc");
```


Показывает, как задать пользовательский тип масштабирования, который более старые версии Microsoft Word применяют к документу при загрузке.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Установите свойство "ZoomType" в "ZoomType.PageWidth", чтобы получить Microsoft Word
// для автоматического масштабирования документа до ширины страницы.
// Установите свойство "ZoomType" в "ZoomType.FullPage", чтобы получить Microsoft Word
// для автоматического масштабирования документа так, чтобы была видна вся первая страница.
// Установите свойство "ZoomType" в "ZoomType.TextFit", чтобы получить Microsoft Word
// для автоматического масштабирования документа до внутренних полей текста первой страницы.
doc->get_ViewOptions()->set_ZoomType(zoomType);

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomType.doc");
```

## См. также

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
