---
title: ViewOptions.DoNotDisplayPageBoundaries
linktitle: DoNotDisplayPageBoundaries
articleTitle: DoNotDisplayPageBoundaries
second_title: Aspose.Words لـ .NET
description: ViewOptions DoNotDisplayPageBoundaries ملكية. إيقاف عرض المسافة بين أعلى النص والحافة العلوية للصفحة في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.settings/viewoptions/donotdisplaypageboundaries/
---
## ViewOptions.DoNotDisplayPageBoundaries property

إيقاف عرض المسافة بين أعلى النص والحافة العلوية للصفحة.

```csharp
public bool DoNotDisplayPageBoundaries { get; set; }
```

## أمثلة

يوضح كيفية إخفاء المسافات البيضاء الرأسية والرؤوس/التذييلات في خيارات العرض.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل محتوى يمتد عبر 3 صفحات.
builder.Writeln("Paragraph 1, Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 2, Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 3, Page 3.");

// أدخل رأسًا وتذييلًا.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the footer.");

// يحتوي هذا المستند على كمية صغيرة من المحتوى تشغل بضع صفحات كاملة من المساحة.
// قم بتعيين علامة "DoNotDisplayPageBoundaries" على "صحيح" لجعل الإصدارات الأقدم من Microsoft Word تحذف الرؤوس،
// التذييلات، والكثير من المسافات البيضاء الرأسية عند عرض وثيقتنا.
// اضبط علامة "DoNotDisplayPageBoundaries" على "خطأ" للحصول على الإصدارات الأقدم من Microsoft Word
// لعرض وثيقتنا بشكل طبيعي.
doc.ViewOptions.DoNotDisplayPageBoundaries = doNotDisplayPageBoundaries;

doc.Save(ArtifactsDir + "ViewOptions.DisplayPageBoundaries.doc");
```

### أنظر أيضا

* class [ViewOptions](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
