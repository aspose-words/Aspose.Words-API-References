---
title: Font.NameBi
linktitle: NameBi
articleTitle: NameBi
second_title: Aspose.Words لـ .NET
description: Font NameBi ملكية. إرجاع أو تعيين اسم الخط في مستند لغة من اليمين إلى اليسار في C#.
type: docs
weight: 250
url: /ar/net/aspose.words/font/namebi/
---
## Font.NameBi property

إرجاع أو تعيين اسم الخط في مستند لغة من اليمين إلى اليسار.

```csharp
public string NameBi { get; set; }
```

## أمثلة

يوضح كيفية تحديد مجموعات منفصلة من إعدادات الخط للنص من اليمين إلى اليسار، ومن اليمين إلى اليسار.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تحديد مجموعة من إعدادات الخط للنص من اليسار إلى اليمين.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// تحديد مجموعة أخرى من إعدادات الخط للنص من اليمين إلى اليسار.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// يمكننا استخدام علامة Bidi للإشارة إلى ما إذا كان النص الذي نحن على وشك إضافته أم لا
// مع منشئ المستندات يكون من اليمين إلى اليسار. عندما نضيف نصًا مع تعيين هذه العلامة على "صحيح"،
// سيتم تنسيقه باستخدام مجموعة إعدادات الخط من اليمين إلى اليسار.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// اضبط العلامة على خطأ، ثم أضف نصًا من اليسار إلى اليمين.
// سيقوم منشئ المستندات بتنسيقها باستخدام مجموعة إعدادات الخط من اليسار إلى اليمين.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### أنظر أيضا

* property [Name](../name/)
* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
