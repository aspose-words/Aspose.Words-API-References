---
title: "طريقة Aspose::Words::PageSetup::get_Margins"
linktitle: "get_Margins"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PageSetup::get_Margins. تُرجِع أو تُعيّن هوامش الصفحة المحددة مسبقًا في C++."
type: docs
weight: 28000
url: /ar/cpp/aspose.words/pagesetup/get_margins/
---
## PageSetup::get_Margins method


تُرجِع أو تُعيّن هوامش [Margins](../../margins/) المحددة مسبقًا للصفحة.

```cpp
Aspose::Words::Margins Aspose::Words::PageSetup::get_Margins()
```


## أمثلة



يظهر متى يجب إعادة حساب تخطيط الصفحة للمستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// حفظ المستند إلى PDF أو إلى صورة أو طباعته للمرة الأولى سيؤدي تلقائيًا
// لتخزين تخطيط المستند داخل صفحاته في الذاكرة المؤقتة.
doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.1.pdf");

// تعديل المستند بطريقة ما.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(6);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
doc->get_Sections()->idx_get(0)->get_PageSetup()->set_Margins(Aspose::Words::Margins::Mirrored);

// في الإصدار الحالي من Aspose.Words، تعديل المستند لا يعيد بناءه تلقائيًا
// تخطيط الصفحة المخزّن مؤقتًا. إذا أردنا أن يكون التخطيط المخزّن مؤقتًا
// للبقاء محدثًا، سنحتاج إلى تحديثه يدويًا.
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Document.UpdatePageLayout.2.pdf");
```

## انظر أيضًا

* Enum [Margins](../../margins/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
