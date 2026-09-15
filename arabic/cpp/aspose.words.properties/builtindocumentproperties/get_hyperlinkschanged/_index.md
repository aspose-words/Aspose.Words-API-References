---
title: "طريقة Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged"
linktitle: "get_HyperlinksChanged"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged. تشير إلى ما إذا تم تغيير الروابط التشعبية في المستند في C++."
type: docs
weight: 13500
url: /ar/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkschanged/
---
## BuiltInDocumentProperties::get_HyperlinksChanged method


يشير إلى ما إذا تم تغيير الروابط في المستند.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged()
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
