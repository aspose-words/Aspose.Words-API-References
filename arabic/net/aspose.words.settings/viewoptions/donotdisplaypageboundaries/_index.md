---
title: ViewOptions.DoNotDisplayPageBoundaries
linktitle: DoNotDisplayPageBoundaries
articleTitle: DoNotDisplayPageBoundaries
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية ViewOptions DoNotDisplayPageBoundaries على تحسين تخطيطك من خلال إزالة مساحة الهامش العلوي للحصول على مظهر أنظف وأكثر احترافية.
type: docs
weight: 20
url: /ar/net/aspose.words.settings/viewoptions/donotdisplaypageboundaries/
---
## ViewOptions.DoNotDisplayPageBoundaries property

يقوم بإيقاف عرض المسافة بين أعلى النص والحافة العلوية للصفحة.

```csharp
public bool DoNotDisplayPageBoundaries { get; set; }
```

## أمثلة

يوضح كيفية إخفاء المسافات الرأسية والرؤوس/التذييلات في خيارات العرض.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إدراج محتوى يمتد عبر 3 صفحات.
builder.Writeln("Paragraph 1, Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 2, Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 3, Page 3.");

//إدراج رأس وتذييل.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the footer.");

// تحتوي هذه الوثيقة على كمية صغيرة من المحتوى الذي يشغل مساحة بضع صفحات كاملة.
// اضبط علامة "DoNotDisplayPageBoundaries" على "true" لجعل الإصدارات القديمة من Microsoft Word تتجاهل الرؤوس،
//التذييلات، والكثير من المسافات الرأسية عند عرض مستندنا.
// اضبط علامة "DoNotDisplayPageBoundaries" على "false" للحصول على الإصدارات الأقدم من Microsoft Word
// لعرض مستندنا بشكل طبيعي.
doc.ViewOptions.DoNotDisplayPageBoundaries = doNotDisplayPageBoundaries;

doc.Save(ArtifactsDir + "ViewOptions.DisplayPageBoundaries.doc");
```

### أنظر أيضا

* class [ViewOptions](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
