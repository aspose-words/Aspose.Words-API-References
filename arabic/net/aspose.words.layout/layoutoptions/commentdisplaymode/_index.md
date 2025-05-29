---
title: LayoutOptions.CommentDisplayMode
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية LayoutOptions CommentDisplayMode لتخصيص عرض التعليقات. اضبطها بسهولة لتحسين تجربة المستخدم باستخدام خيارات مثل ShowInBalloons.
type: docs
weight: 30
url: /ar/net/aspose.words.layout/layoutoptions/commentdisplaymode/
---
## LayoutOptions.CommentDisplayMode property

يحصل على طريقة عرض التعليقات أو يعينها. القيمة الافتراضية هيShowInBalloons .

```csharp
public CommentDisplayMode CommentDisplayMode { get; set; }
```

## ملاحظات

لاحظ أن المراجعات لا يتم تقديمها في البالونات لـShowInAnnotations .

## أمثلة

يوضح كيفية إظهار التعليقات عند حفظ مستند بتنسيق مُقدم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

//يتوفر ShowInAnnotations فقط بتنسيقي Pdf1.7 وPdf1.5.
// في التنسيقات الأخرى، سوف يعمل بشكل مشابه لإخفاء.
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
