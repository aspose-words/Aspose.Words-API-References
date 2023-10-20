---
title: LayoutOptions.CommentDisplayMode
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words لـ .NET
description: LayoutOptions CommentDisplayMode ملكية. الحصول على أو تعيين الطريقة التي يتم بها عرض التعليقات. القيمة الافتراضية هيShowInBalloons  في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.layout/layoutoptions/commentdisplaymode/
---
## LayoutOptions.CommentDisplayMode property

الحصول على أو تعيين الطريقة التي يتم بها عرض التعليقات. القيمة الافتراضية هيShowInBalloons .

```csharp
public CommentDisplayMode CommentDisplayMode { get; set; }
```

## ملاحظات

لاحظ أنه لا يتم عرض المراجعات في بالوناتShowInAnnotations .

## أمثلة

يوضح كيفية إظهار التعليقات عند حفظ مستند بتنسيق معروض.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations متاح فقط بتنسيقات Pdf1.7 وPdf1.5.
// في التنسيقات الأخرى، سيعمل بشكل مشابه لـ Hide.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInAnnotations;

doc.Save(ArtifactsDir + "Document.ShowCommentsInAnnotations.pdf");

// لاحظ أنه مطلوب إعادة بناء تخطيط صفحة المستند (عبر طريقة Document.UpdatePageLayout())
// بعد تغيير قيم Document.LayoutOptions.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInBalloons;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.ShowCommentsInBalloons.pdf");
```

### أنظر أيضا

* enum [CommentDisplayMode](../../commentdisplaymode/)
* class [LayoutOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
