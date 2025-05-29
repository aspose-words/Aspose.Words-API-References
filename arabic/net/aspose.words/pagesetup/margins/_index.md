---
title: PageSetup.Margins
linktitle: Margins
articleTitle: Margins
second_title: Aspose.Words لـ .NET
description: اضبط هوامش صفحتك بسهولة باستخدام خاصية "إعداد الصفحة". خصّص الإعدادات للحصول على تصميم وعرض مثاليين. حسّن مظهر مستندك!
type: docs
weight: 260
url: /ar/net/aspose.words/pagesetup/margins/
---
## PageSetup.Margins property

إرجاع أو تعيين الإعداد المسبق[`Margins`](../../margins/) من الصفحة.

```csharp
public Margins Margins { get; set; }
```

## أمثلة

يُظهر متى يجب إعادة حساب تخطيط الصفحة للمستند.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// سيتم حفظ المستند بتنسيق PDF، أو إلى صورة، أو طباعته لأول مرة تلقائيًا
// تخزين تخطيط المستند داخل صفحاته.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

//تعديل المستند بطريقة ما.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

// في الإصدار الحالي من Aspose.Words، لا يؤدي تعديل المستند إلى إعادة البناء تلقائيًا
// تخطيط الصفحة المُخزّن مؤقتًا. إذا أردنا تخطيطًا مُخزّنًا مؤقتًا
//للبقاء على اطلاع، سوف نحتاج إلى تحديثه يدويًا.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### أنظر أيضا

* enum [Margins](../../margins/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
