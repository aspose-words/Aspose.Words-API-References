---
title: CommentDisplayMode Enum
linktitle: CommentDisplayMode
articleTitle: CommentDisplayMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.Layout.CommentDisplayMode لتحسين عرض تعليقات المستندات. حسّن وضوح مستندك وعرضه اليوم!
type: docs
weight: 3740
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
| Hide | `0` | لم يتم تقديم أي تعليقات على المستند. |
| ShowInBalloons | `1` | يعرض تعليقات المستند في بالونات في الهامش. هذه هي القيمة الافتراضية. |
| ShowInAnnotations | `2` | يعرض تعليقات المستندات في شكل شروح توضيحية. هذا متاح فقط لصيغة PDF. |

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

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)
