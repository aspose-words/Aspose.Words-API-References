---
title: Document.UpdatePageLayout
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. يعيد بناء تخطيط الصفحة للمستند.
type: docs
weight: 790
url: /ar/net/aspose.words/document/updatepagelayout/
---
## Document.UpdatePageLayout method

يعيد بناء تخطيط الصفحة للمستند.

```csharp
public void UpdatePageLayout()
```

### ملاحظات

تقوم هذه الطريقة بتنسيق المستند إلى صفحات وتحديث الحقول ذات الصلة برقم الصفحة في المستند مثل مثل PAGE وPAGES وPAGEREF وREF. معلومات تخطيط الصفحة المحدثة مطلوبة للعرض الصحيح للمستند إلى تنسيقات الصفحات الثابتة.

يتم استدعاء هذه الطريقة تلقائيًا عندما تقوم لأول مرة بتحويل مستند إلى PDF أو XPS أو صورة أو طباعته. ومع ذلك، إذا قمت بتعديل المستند بعد عرضه ثم حاولت عرضه مرة أخرى - فلن يقوم Aspose.Words بتحديث تخطيط الصفحة تلقائيًا. في هذه الحالة يجب عليك الاتصال`UpdatePageLayout` قبل العرض مرة أخرى.

### أمثلة

يوضح متى يجب إعادة حساب تخطيط صفحة المستند.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// سيتم تلقائيًا حفظ مستند إلى PDF أو صورة أو طباعته لأول مرة
// قم بتخزين تخطيط المستند داخل صفحاته.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// قم بتعديل المستند بطريقة ما.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

 // في الإصدار الحالي من Aspose.Words، لا يؤدي تعديل المستند إلى إعادة البناء تلقائيًا
// تخطيط الصفحة المخزنة مؤقتًا. إذا أردنا التخطيط المخبأ
// للبقاء على اطلاع، سنحتاج إلى تحديثه يدويًا.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


