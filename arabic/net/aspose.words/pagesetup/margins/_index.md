---
title: PageSetup.Margins
second_title: Aspose.Words لمراجع .NET API
description: PageSetup ملكية. إرجاع أو ضبط الإعداد المسبقMargins من الصفحة.
type: docs
weight: 260
url: /ar/net/aspose.words/pagesetup/margins/
---
## PageSetup.Margins property

إرجاع أو ضبط الإعداد المسبق[`Margins`](../../margins/) من الصفحة.

```csharp
public Margins Margins { get; set; }
```

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

* enum [Margins](../../margins/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../pagesetup/)
* المجسم [Aspose.Words](../../../)


