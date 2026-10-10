---
title: "Aspose::Words::Margins enum"
linktitle: "الهوامش"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Margins enum. يحدد الهوامش المحددة مسبقًا في C++."
type: docs
weight: 99000
url: /ar/cpp/aspose.words/margins/
---
## Margins enum


يحدد الهوامش المحددة مسبقًا.

```cpp
enum class Margins
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| عادي | 0 | هوامش عادية. |
| ضيق | 1 | هوامش ضيقة. |
| متوسط | 2 | هوامش متوسطة. |
| واسع | 3 | هوامش واسعة. |
| معكوسة | 4 | هوامش معكوسة. |
| مخصص | 5 | هوامش مخصصة. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
