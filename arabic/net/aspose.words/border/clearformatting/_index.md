---
title: Border.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words لـ .NET
description: أعد ضبط خصائص حدودك إلى الوضع الافتراضي باستخدام طريقة Border ClearFormatting. بسّط عملية التصميم وحسّن مظهر مشروعك!
type: docs
weight: 90
url: /ar/net/aspose.words/border/clearformatting/
---
## Border.ClearFormatting method

إعادة تعيين خصائص الحدود إلى القيم الافتراضية.

```csharp
public void ClearFormatting()
```

## ملاحظات

عند إعادة تعيين خصائص الحدود إلى القيم الافتراضية، تصبح الحدود غير مرئية.

## أمثلة

يوضح كيفية إزالة الحدود من فقرة.

```csharp
Document doc = new Document(MyDir + "Borders.docx");

//تحتوي كل فقرة على مجموعة فردية من الحدود.
//يمكننا الوصول إلى إعدادات مظهر هذه الحدود عبر كائن تنسيق الفقرة.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;

Assert.AreEqual(Color.Red.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(3.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.Single, borders[0].LineStyle);
Assert.True(borders[0].IsVisible);

 //يمكننا إزالة الحدود مرة واحدة عن طريق تشغيل طريقة ClearFormatting.
// سيؤدي تشغيل هذه الطريقة على كل حدود الفقرة إلى إزالة جميع حدودها.
foreach (Border border in borders)
    border.ClearFormatting();

Assert.AreEqual(Color.Empty.ToArgb(), borders[0].Color.ToArgb());
Assert.AreEqual(0.0d, borders[0].LineWidth);
Assert.AreEqual(LineStyle.None, borders[0].LineStyle);
Assert.IsFalse(borders[0].IsVisible);

doc.Save(ArtifactsDir + "Border.ClearFormatting.docx");
```

### أنظر أيضا

* class [Border](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
