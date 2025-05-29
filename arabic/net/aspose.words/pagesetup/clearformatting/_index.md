---
title: PageSetup.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words لـ .NET
description: أعد ضبط إعدادات صفحات مستندك بسهولة باستخدام طريقة ClearFormatting. استعد الهوامش الافتراضية وحجم الورق والاتجاه لمظهر أنيق.
type: docs
weight: 460
url: /ar/net/aspose.words/pagesetup/clearformatting/
---
## PageSetup.ClearFormatting method

إعادة تعيين إعدادات الصفحة إلى حجم الورق والهوامش والاتجاه الافتراضي.

```csharp
public void ClearFormatting()
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

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
