---
title: "Aspose::Words::Settings::ZoomType enum"
linktitle: "ZoomType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::ZoomType enum. Возможные значения, определяющие, насколько крупно или мелко документ отображается на экране в Microsoft Word в C++."
type: docs
weight: 22000
url: /ru/cpp/aspose.words.settings/zoomtype/
---
## ZoomType enum


Возможные значения того, насколько большой или маленький документ отображается на экране в Microsoft Word.

```cpp
enum class ZoomType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Пользовательский | 0 | Процент масштабирования задаётся явно. Он не пересчитывается автоматически при изменении размера элемента управления. |
| None | n/a | Указывает использовать явный процент масштабирования. То же, что и [Custom](./). |
| FullPage | 1 | Процент масштабирования автоматически пересчитывается, чтобы поместить одну полную страницу. |
| PageWidth | 2 | Процент масштабирования автоматически пересчитывается, чтобы соответствовать ширине страницы. |
| TextFit | 3 | Процент масштабирования автоматически пересчитывается, чтобы соответствовать тексту. |


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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
