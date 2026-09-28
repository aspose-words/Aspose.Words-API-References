---
title: "Aspose::Words::StyleCollection::ClearQuickStyleGallery метод"
linktitle: "ClearQuickStyleGallery"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::StyleCollection::ClearQuickStyleGallery метод. Удаляет все стили из панели быстрой галереи стилей в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/stylecollection/clearquickstylegallery/
---
## StyleCollection::ClearQuickStyleGallery method


Удаляет все стили из панели быстрой [Стиль](../../style/) галереи.

```cpp
void Aspose::Words::StyleCollection::ClearQuickStyleGallery()
```


## Примеры



Показывает, как удалить стили из панели галереи [Стиль](../../style/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
// Обратите внимание, что удаление стилей пока работает только с форматом DOCX.
doc->get_Styles()->ClearQuickStyleGallery();

doc->Save(get_ArtifactsDir() + u"Styles.RemoveStylesFromStyleGallery.docx");
```

## См. также

* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
