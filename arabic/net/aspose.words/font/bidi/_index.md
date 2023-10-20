---
title: Font.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words لـ .NET
description: Font Bidi ملكية. يحدد ما إذا كانت محتويات هذا التشغيل يجب أن تكون ذات خصائص من اليمين إلى اليسار في C#.
type: docs
weight: 30
url: /ar/net/aspose.words/font/bidi/
---
## Font.Bidi property

يحدد ما إذا كانت محتويات هذا التشغيل يجب أن تكون ذات خصائص من اليمين إلى اليسار.

```csharp
public bool Bidi { get; set; }
```

## ملاحظات

لا يجوز استخدام هذه الخاصية، عند تشغيلها، مع نص من اليسار إلى اليمين بشدة. أي سلوك في ظل هذا الشرط غير محدد. لا يجوز استخدام هذه الخاصية، عند إيقاف تشغيلها، مع نص قوي من اليمين إلى اليسار. أي سلوك في ظل هذا الشرط غير محدد.

عندما يتم عرض محتويات هذا التشغيل، يجب التعامل مع كافة الأحرف كأحرف نصية معقدة لأغراض formatting . هذا يعني ذاك[`BoldBi`](../boldbi/) ,[`ItalicBi`](../italicbi/) ,[`SizeBi`](../sizebi/) وسيتم استخدام الخط المقابل name عند عرض هذا التشغيل.

أيضًا، عند عرض محتويات هذا التشغيل، تعمل هذه الخاصية كتجاوز من اليمين إلى اليسار لـ Characters والتي تم تصنيفها على أنها "أنواع ضعيفة" و"أنواع محايدة".

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

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
