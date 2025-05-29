---
title: Style.AutomaticallyUpdate
linktitle: AutomaticallyUpdate
articleTitle: AutomaticallyUpdate
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية AutomaticallyUpdate على تعزيز أنماطك من خلال إعادة تعريفها تلقائيًا للحصول على القيمة والأداء الأمثل في مشاريعك.
type: docs
weight: 20
url: /ar/net/aspose.words/style/automaticallyupdate/
---
## Style.AutomaticallyUpdate property

يحدد ما إذا كان سيتم إعادة تعريف هذا النمط تلقائيًا استنادًا إلى القيمة المناسبة.

```csharp
public bool AutomaticallyUpdate { get; set; }
```

## ملاحظات

إذا تم تعيين قيمة الخاصية على true، يقوم MS Word تلقائيًا بإعادة تعريف النمط الحالي عندما يتم تغيير تنسيق الفقرة المناسب.

تنطبق خاصية التحديث التلقائي على أنماط الفقرة فقط.

القيمة الافتراضية هي`خطأ شنيع`.

## أمثلة

يوضح كيفية إنشاء نمط مخصص وتطبيقه.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
//إعادة تعريف النمط تلقائيًا.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتطبيق أحد الأنماط الموجودة في المستند على الفقرة التي يقوم منشئ المستند بإنشائها.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// قم بإزالة النمط المخصص لدينا من مجموعة أنماط المستند.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// أي نص يستخدم نمطًا تمت إزالته يعود إلى التنسيق الافتراضي.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### أنظر أيضا

* class [Style](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
