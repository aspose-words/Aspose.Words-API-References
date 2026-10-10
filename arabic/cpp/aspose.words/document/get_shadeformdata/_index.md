---
title: "طريقة Aspose::Words::Document::get_ShadeFormData"
linktitle: "get_ShadeFormData"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_ShadeFormData. يحدد ما إذا كان يجب تشغيل التظليل الرمادي على حقول النموذج في C++."
type: docs
weight: 49000
url: /ar/cpp/aspose.words/document/get_shadeformdata/
---
## Document::get_ShadeFormData method


يحدد ما إذا كان سيتم تشغيل التظليل الرمادي على حقول النموذج.

```cpp
bool Aspose::Words::Document::get_ShadeFormData()
```


## أمثلة



يوضح كيفية تطبيق التظليل الرمادي على حقول النموذج.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world! ");
builder->InsertTextInput(u"My form field", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Text contents of form field, which are shaded in grey by default.", 0);

// يمكننا إيقاف تشغيل التظليل الرمادي، بحيث يندمج النص المعلَّم مع النص الآخر.
doc->set_ShadeFormData(useGreyShading);
doc->Save(get_ArtifactsDir() + u"Document.ShadeFormData.docx");
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
