---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop طريقة"
linktitle: "get_ScaleCrop"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop طريقة. يوضح ما إذا كان مصغّر المستند مقصوصًا أو مُقاسًا ليتناسب مع العرض في C++."
type: docs
weight: 24500
url: /ar/cpp/aspose.words.properties/builtindocumentproperties/get_scalecrop/
---
## BuiltInDocumentProperties::get_ScaleCrop method


يشير إلى ما إذا كان مصغّر المستند مقصوصاً أو مُقاساً ليتناسب مع العرض.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop()
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
