---
title: "Aspose::Words::Settings::ViewOptions::get_ViewType метод"
linktitle: "get_ViewType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::ViewOptions::get_ViewType метод. Управляет режимом просмотра в Microsoft Word в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.settings/viewoptions/get_viewtype/
---
## ViewOptions::get_ViewType method


Управляет режимом просмотра в Microsoft Word.

```cpp
Aspose::Words::Settings::ViewType Aspose::Words::Settings::ViewOptions::get_ViewType() const
```

## Примечания


Хотя Aspose.Words может читать и записывать эту опцию, её использование зависит от конкретного приложения. Например, MS Word 2013 не учитывает значение этой опции.

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

## См. также

* Enum [ViewType](../../viewtype/)
* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
