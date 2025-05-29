---
title: Font.LocaleIdBi
linktitle: LocaleIdBi
articleTitle: LocaleIdBi
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Font LocaleIdBi، وقم بإدارة معرفات الإعدادات المحلية بسهولة للأحرف المنسقة من اليمين إلى اليسار، مما يعزز تطبيقاتك متعددة اللغات.
type: docs
weight: 210
url: /ar/net/aspose.words/font/localeidbi/
---
## Font.LocaleIdBi property

يحصل على معرف الإعدادات المحلية (اللغة) للأحرف المنسقة من اليمين إلى اليسار أو يعينه.

```csharp
public int LocaleIdBi { get; set; }
```

## ملاحظات

للحصول على قائمة بمعرفات الإعدادات المحلية، راجع https://msdn.microsoft.com/en-us/library/cc233965.aspx

## أمثلة

يوضح كيفية تحديد مجموعات منفصلة من إعدادات الخط للنص من اليمين إلى اليسار، ومن اليمين إلى اليسار.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتحديد مجموعة من إعدادات الخط للنص من اليسار إلى اليمين.
builder.Font.Name = "Courier New";
builder.Font.Size = 16;
builder.Font.Italic = false;
builder.Font.Bold = false;
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// قم بتعريف مجموعة أخرى من إعدادات الخط للنص من اليمين إلى اليسار.
builder.Font.NameBi = "Andalus";
builder.Font.SizeBi = 24;
builder.Font.ItalicBi = true;
builder.Font.BoldBi = true;
builder.Font.LocaleIdBi = new CultureInfo("ar-AR", false).LCID;

// يمكننا استخدام علم Bidi للإشارة إلى ما إذا كان النص الذي سنضيفه
// مع مُنشئ المستندات، يكون الاتجاه من اليمين إلى اليسار. عند إضافة نص مع ضبط هذه العلامة على "صحيح"،
//سيتم تنسيقه باستخدام مجموعة إعدادات الخط من اليمين إلى اليسار.
builder.Font.Bidi = true;
builder.Write("مرحبًا");

// قم بضبط العلم على false، ثم قم بإضافة نص من اليسار إلى اليمين.
// سيقوم منشئ المستندات بتنسيق هذه العناصر باستخدام مجموعة إعدادات الخط من اليسار إلى اليمين.
builder.Font.Bidi = false;
builder.Write(" Hello world!");

doc.Save(ArtifactsDir + "Font.Bidi.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
