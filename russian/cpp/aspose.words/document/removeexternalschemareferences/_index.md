---
title: "Aspose::Words::Document::RemoveExternalSchemaReferences метод"
linktitle: "RemoveExternalSchemaReferences"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::RemoveExternalSchemaReferences метод. Удаляет внешние ссылки на XML‑схемы из этого документа в C++."
type: docs
weight: 68000
url: /ru/cpp/aspose.words/document/removeexternalschemareferences/
---
## Document::RemoveExternalSchemaReferences method


Удаляет внешние ссылки на XML‑схемы из этого документа.

```cpp
void Aspose::Words::Document::RemoveExternalSchemaReferences()
```


## Примеры



Показывает, как удалить все внешние ссылки на XML‑схемы из документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"External XML schema.docx");

doc->RemoveExternalSchemaReferences();
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
