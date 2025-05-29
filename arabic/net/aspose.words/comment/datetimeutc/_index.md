---
title: Comment.DateTimeUtc
linktitle: DateTimeUtc
articleTitle: DateTimeUtc
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Comment DateTimeUtc، التي تقوم باسترداد تاريخ ووقت UTC الدقيق لتعليقاتك من أجل التتبع والإدارة الدقيقة.
type: docs
weight: 50
url: /ar/net/aspose.words/comment/datetimeutc/
---
## Comment.DateTimeUtc property

يحصل على تاريخ ووقت UTC الذي تم فيه تقديم التعليق.

```csharp
public DateTime DateTimeUtc { get; }
```

## ملاحظات

القيمة الافتراضية هي MinValue

## أمثلة

يوضح كيفية الحصول على تاريخ ووقت UTC.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

DateTime dateTime = DateTime.Now;
Comment comment = new Comment(doc, "John Doe", "J.D.", dateTime);
comment.SetText("My comment.");

builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.UtcDateTime.docx");
doc = new Document(ArtifactsDir + "Comment.UtcDateTime.docx");

comment = (Comment)doc.GetChild(NodeType.Comment, 0, true);
// DateTimeUtc يقوم بإرجاع البيانات بدون مللي ثانية.
Assert.AreEqual(dateTime.ToUniversalTime().ToString("yyyy-MM-dd hh:mm:ss"), comment.DateTimeUtc.ToString("yyyy-MM-dd hh:mm:ss"));
```

### أنظر أيضا

* class [Comment](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
