---
title: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent method"
linktitle: "get_ZoomPercent"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent method. Получает или задает процент масштабирования, с которым вы хотите просматривать документ в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.settings/viewoptions/get_zoompercent/
---
## ViewOptions::get_ZoomPercent method


Получает или задает процент, с которым вы хотите просматривать документ.

```cpp
int32_t Aspose::Words::Settings::ViewOptions::get_ZoomPercent() const
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

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
