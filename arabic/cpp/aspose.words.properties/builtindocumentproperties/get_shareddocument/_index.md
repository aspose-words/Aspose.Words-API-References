---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument طريقة"
linktitle: "get_SharedDocument"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument طريقة. يشير إلى ما إذا كان المستند مستندًا مشتركًا في C++."
type: docs
weight: 25500
url: /ar/cpp/aspose.words.properties/builtindocumentproperties/get_shareddocument/
---
## BuiltInDocumentProperties::get_SharedDocument method


يشير إلى ما إذا كان المستند مستنداً مشتركاً.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument()
```

## ملاحظات


Aspose.Words لا يقوم بتحديث هذه الخاصية.

## أمثلة



يعرض كيفية الحصول على الخصائص الموسعة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Extended properties.docx");
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_ScaleCrop());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_SharedDocument());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_HyperlinksChanged());
```

## انظر أيضًا

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
