---
title: "Aspose::Words::Document::get_ViewOptions метод"
linktitle: "get_ViewOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::get_ViewOptions метод. Предоставляет параметры для управления тем, как документ отображается в Microsoft Word в C++."
type: docs
weight: 58000
url: /ru/cpp/aspose.words/document/get_viewoptions/
---
## Document::get_ViewOptions method


Предоставляет параметры для управления тем, как документ отображается в Microsoft Word.

```cpp
System::SharedPtr<Aspose::Words::Settings::ViewOptions> Aspose::Words::Document::get_ViewOptions()
```


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

* Class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
