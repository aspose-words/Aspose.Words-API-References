---
title: PageSetup.VerticalAlignment
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية VerticalAlignment في PageSetup على تحسين تخطيط المستند من خلال ضبط محاذاة النص لتحسين قابلية القراءة والعرض.
type: docs
weight: 450
url: /ar/net/aspose.words/pagesetup/verticalalignment/
---
## PageSetup.VerticalAlignment property

يعيد أو يضبط المحاذاة الرأسية للنص في كل صفحة في مستند أو قسم.

```csharp
public PageVerticalAlignment VerticalAlignment { get; set; }
```

## أمثلة

يوضح كيفية تطبيق إعدادات إعداد الصفحة وإعادتها إلى الأقسام في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعديل خصائص إعداد الصفحة للقسم الحالي للمنشئ وإضافة نص.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// إذا بدأنا قسمًا جديدًا باستخدام منشئ المستندات،
// سوف يرث خصائص إعداد الصفحة الحالية للمنشئ.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// يمكننا إرجاع خصائص إعداد الصفحة إلى قيمها الافتراضية باستخدام طريقة "ClearFormatting".
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### أنظر أيضا

* enum [PageVerticalAlignment](../../pageverticalalignment/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
