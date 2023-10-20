---
title: Style.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words لـ .NET
description: Style Font ملكية. الحصول على تنسيق الأحرف للنمط في C#.
type: docs
weight: 60
url: /ar/net/aspose.words/style/font/
---
## Style.Font property

الحصول على تنسيق الأحرف للنمط.

```csharp
public Font Font { get; }
```

## ملاحظات

بالنسبة لأنماط القائمة، تُرجع هذه الخاصية`باطل`.

## أمثلة

يوضح كيفية إنشاء نمط فقرة واستخدامه بتنسيق القائمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء نمط فقرة مخصص.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// أنشئ قائمة وتأكد من أن الفقرات التي تستخدم هذا النمط ستستخدم هذه القائمة.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// قم بتطبيق نمط الفقرة على الفقرة الحالية لمنشئ المستند، ثم قم بإضافة بعض النص.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// قم بتغيير نمط منشئ المستندات إلى نمط لا يحتوي على تنسيق قائمة واكتب فقرة أخرى.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

يوضح كيفية إنشاء نمط مخصص وتطبيقه.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// إعادة تعريف النمط تلقائيًا.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتطبيق أحد الأنماط من المستند على الفقرة التي يقوم منشئ المستند بإنشائها.
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

* class [Font](../../font/)
* class [Style](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
