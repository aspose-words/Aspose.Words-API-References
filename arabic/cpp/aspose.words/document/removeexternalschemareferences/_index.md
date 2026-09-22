---
title: "طريقة Aspose::Words::Document::RemoveExternalSchemaReferences"
linktitle: "RemoveExternalSchemaReferences"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::RemoveExternalSchemaReferences. يزيل مراجع مخطط XML الخارجية من هذا المستند في C++."
type: docs
weight: 68000
url: /ar/cpp/aspose.words/document/removeexternalschemareferences/
---
## Document::RemoveExternalSchemaReferences method


يزيل مراجع مخطط XML الخارجية من هذا المستند.

```cpp
void Aspose::Words::Document::RemoveExternalSchemaReferences()
```


## أمثلة



يوضح كيفية إزالة جميع مراجع مخطط XML الخارجية من مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"External XML schema.docx");

doc->RemoveExternalSchemaReferences();
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
