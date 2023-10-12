---
title: Font.SizeBi
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. الحصول على حجم الخط أو تعيينه بالنقاط المستخدمة في مستند من اليمين إلى اليسار.
type: docs
weight: 350
url: /ar/net/aspose.words/font/sizebi/
---
## Font.SizeBi property

الحصول على حجم الخط أو تعيينه بالنقاط المستخدمة في مستند من اليمين إلى اليسار.

```csharp
public double SizeBi { get; set; }
```

### أمثلة

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

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


