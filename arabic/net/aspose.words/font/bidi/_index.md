---
title: Font.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Font Bidi، وتحكم في خصائص النص من اليمين إلى اليسار لتحسين قابلية القراءة وتجربة المستخدم في تصميمات الويب الخاصة بك.
type: docs
weight: 30
url: /ar/net/aspose.words/font/bidi/
---
## Font.Bidi property

يحدد ما إذا كان محتوى هذا التشغيل يجب أن يحتوي على خصائص من اليمين إلى اليسار.

```csharp
public bool Bidi { get; set; }
```

## ملاحظات

هذه الخاصية، عند تفعيلها، لا تُستخدم مع النصوص ذات الاتجاه القوي من اليسار إلى اليمين. أي سلوك في ظل هذا الشرط غير محدد. هذه الخاصية، عند إيقافها، لا تُستخدم مع النصوص ذات الاتجاه القوي من اليمين إلى اليسار. أي سلوك في ظل هذا الشرط غير محدد.

عند عرض محتويات هذا التشغيل، سيتم التعامل مع جميع الأحرف كأحرف نصية معقدة لأغراض formatting . هذا يعني أن[`BoldBi`](../boldbi/) ،[`ItalicBi`](../italicbi/) ،[`SizeBi`](../sizebi/) وسيتم استخدام الخط المقابل name عند عرض هذا التشغيل.

بالإضافة إلى ذلك، عندما يتم عرض محتويات هذا التشغيل، تعمل هذه الخاصية كتجاوز من اليمين إلى اليسار لـ characters والتي يتم تصنيفها على أنها "أنواع ضعيفة" و"أنواع محايدة".

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
