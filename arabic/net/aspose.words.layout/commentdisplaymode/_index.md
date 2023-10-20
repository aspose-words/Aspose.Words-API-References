---
title: CommentDisplayMode Enum
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Layout.CommentDisplayMode تعداد. يحدد وضع العرض لتعليقات المستند في C#.
type: docs
weight: 3290
url: /ar/net/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enumeration

يحدد وضع العرض لتعليقات المستند.

```csharp
public enum CommentDisplayMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Hide | `0` | لم يتم عرض أي تعليقات على المستند. |
| ShowInBalloons | `1` | يعرض تعليقات المستند في بالونات في الهامش. هذه هي القيمة الافتراضية. |
| ShowInAnnotations | `2` | يعرض تعليقات المستند في التعليقات التوضيحية. هذا متاح فقط لتنسيق Pdf. |

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

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)
