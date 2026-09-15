---
title: "Aspose::Words::Document::get_PageCount طريقة"
linktitle: "get_PageCount"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Document::get_PageCount طريقة. يحصل على عدد الصفحات في المستند كما تم حسابه بواسطة أحدث عملية تخطيط للصفحة في C++."
type: docs
weight: 43000
url: /ar/cpp/aspose.words/document/get_pagecount/
---
## Document::get_PageCount method


يحصل على عدد الصفحات في المستند كما تم حسابه بواسطة أحدث عملية تخطيط للصفحة.

```cpp
int32_t Aspose::Words::Document::get_PageCount()
```


## أمثلة



يظهر كيفية عد عدد الصفحات في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Page 1");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Page 3");

// تحقق من عدد الصفحات المتوقع في المستند.
ASSERT_EQ(3, doc->get_PageCount());

// استدعاء خاصية PageCount أدى إلى تشغيل تخطيط صفحة المستند لحساب القيمة.
// لن تحتاج هذه العملية إلى إعادة تنفيذها عند تصيير المستند إلى تنسيق حفظ صفحة ثابت،
// مثل .pdf. لذا يمكنك توفير بعض الوقت، خاصةً مع المستندات الأكثر تعقيدًا.
doc->Save(get_ArtifactsDir() + u"Document.GetPageCount.pdf");
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
