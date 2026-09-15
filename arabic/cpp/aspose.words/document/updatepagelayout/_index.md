---
title: "طريقة Aspose::Words::Document::UpdatePageLayout"
linktitle: "UpdatePageLayout"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::UpdatePageLayout. يعيد بناء تخطيط الصفحات للمستند في C++."
type: docs
weight: 98000
url: /ar/cpp/aspose.words/document/updatepagelayout/
---
## Document::UpdatePageLayout method


يعيد بناء تخطيط الصفحات للمستند.

```cpp
void Aspose::Words::Document::UpdatePageLayout()
```

## ملاحظات


هذه الطريقة تقوم بتنسيق المستند إلى صفحات وتحديث الحقول المتعلقة بأرقام الصفحات في المستند مثل PAGE وPAGES وPAGEREF وREF. المعلومات الحديثة لتخطيط الصفحات ضرورية لتص rendering الصحيح للمستند إلى صيغ الصفحات الثابتة.

يتم استدعاء هذه الطريقة تلقائيًا عند تحويل المستند لأول مرة إلى PDF أو XPS أو صورة أو طباعته. ومع ذلك، إذا قمت بتعديل المستند بعد العرض ثم حاولت عرضه مرة أخرى - لن تقوم Aspose.Words بتحديث تخطيط الصفحات تلقائيًا. في هذه الحالة يجب استدعاء [UpdatePageLayout](./) قبل العرض مرة أخرى.

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
