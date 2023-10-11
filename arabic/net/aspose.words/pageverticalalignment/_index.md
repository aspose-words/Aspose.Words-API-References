---
title: Enum PageVerticalAlignment
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.PageVerticalAlignment تعداد. يحدد الضبط الرأسي للنص في كل صفحة.
type: docs
weight: 4370
url: /ar/net/aspose.words/pageverticalalignment/
---
## PageVerticalAlignment enumeration

يحدد الضبط الرأسي للنص في كل صفحة.

```csharp
public enum PageVerticalAlignment
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Bottom | `3` | تتم محاذاة النص في أسفل الصفحة. |
| Center | `1` | تمت محاذاة النص في منتصف الصفحة. |
| Justify | `2` | النص منتشر لملء الصفحة. |
| Top | `0` | تتم محاذاة النص في أعلى الصفحة. |

### أمثلة

يوضح كيفية تطبيق إعدادات إعداد الصفحة وإعادتها إلى الأقسام الموجودة في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعديل خصائص إعداد الصفحة للقسم الحالي للمنشئ وإضافة نص.
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.VerticalAlignment = PageVerticalAlignment.Center;
builder.Writeln("This is the first section, which landscape oriented with vertically centered text.");

// إذا بدأنا قسمًا جديدًا باستخدام أداة إنشاء المستندات،
// سوف يرث خصائص إعداد الصفحة الحالية للمنشئ.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(Orientation.Landscape, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Center, doc.Sections[1].PageSetup.VerticalAlignment);

// يمكننا إعادة خصائص إعداد الصفحة إلى قيمها الافتراضية باستخدام طريقة "ClearFormatting".
builder.PageSetup.ClearFormatting();

Assert.AreEqual(Orientation.Portrait, doc.Sections[1].PageSetup.Orientation);
Assert.AreEqual(PageVerticalAlignment.Top, doc.Sections[1].PageSetup.VerticalAlignment);

builder.Writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc.Save(ArtifactsDir + "PageSetup.ClearFormatting.docx");
```

### أنظر أيضا

* class [PageSetup](../pagesetup/)
* property [VerticalAlignment](../pagesetup/verticalalignment/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


