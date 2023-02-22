---
title: Enum CommentDisplayMode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Layout.CommentDisplayMode تعداد. يحدد وضع التجسيد لتعليقات المستند.
type: docs
weight: 3090
url: /ar/net/aspose.words.layout/commentdisplaymode/
---
## CommentDisplayMode enumeration

يحدد وضع التجسيد لتعليقات المستند.

```csharp
public enum CommentDisplayMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Hide | `0` | لا يتم تقديم أي تعليقات على المستند. |
| ShowInBalloons | `1` | يتم عرض تعليقات المستند في بالونات في الهامش. هذه هي القيمة الافتراضية. |
| ShowInAnnotations | `2` | يعرض تعليقات المستند في التعليقات التوضيحية. هذا متاح فقط لتنسيق Pdf . |

### أمثلة

يوضح كيفية إظهار التعليقات عند حفظ مستند بتنسيق معروض.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");
builder.CurrentParagraph.AppendChild(comment);

// ShowInAnnotations متاح فقط في تنسيقات Pdf1.7 و Pdf1.5.
// في تنسيقات أخرى ، ستعمل بشكل مشابه لإخفاء.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInAnnotations;

doc.Save(ArtifactsDir + "Document.ShowCommentsInAnnotations.pdf");

// لاحظ أنه يلزم إعادة بناء تخطيط صفحة المستند (عبر طريقة Document.UpdatePageLayout ())
// بعد تغيير قيم Document.LayoutOptions.
doc.LayoutOptions.CommentDisplayMode = CommentDisplayMode.ShowInBalloons;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.ShowCommentsInBalloons.pdf");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Layout](../../aspose.words.layout/)
* المجسم [Aspose.Words](../../)


