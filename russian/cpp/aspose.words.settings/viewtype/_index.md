---
title: "Aspose::Words::Settings::ViewType перечисление"
linktitle: "ViewType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::ViewType перечисление. Возможные значения режима просмотра в Microsoft Word на C++."
type: docs
weight: 21000
url: /ru/cpp/aspose.words.settings/viewtype/
---
## ViewType enum


Возможные значения режима просмотра в Microsoft Word.

```cpp
enum class ViewType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Документ будет отображён в представлении по умолчанию приложения. |
| Reading | 0 | Документ будет отображён в представлении по умолчанию приложения. |
| PageLayout | 1 | Документ будет открыт в представлении, отображающем документ так, как он будет печататься. |
| Outline | 3 | Документ будет отображён в представлении, оптимизированном для создания структуры или работы с длинными документами. |
| Обычный | 4 | Документ будет отображён в представлении, оптимизированном для создания структуры или работы с длинными документами. |
| Web | 5 | Документ будет отображён в представлении, имитирующем способ отображения этого документа на веб‑странице. |


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
