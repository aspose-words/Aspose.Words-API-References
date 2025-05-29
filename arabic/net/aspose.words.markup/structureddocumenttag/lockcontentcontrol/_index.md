---
title: StructuredDocumentTag.LockContentControl
linktitle: LockContentControl
articleTitle: LockContentControl
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية StructuredDocumentTag LockContentControl أمان المستندات من خلال منع المستخدمين من حذف المحتوى المهم. تعرّف على المزيد!
type: docs
weight: 190
url: /ar/net/aspose.words.markup/structureddocumenttag/lockcontentcontrol/
---
## StructuredDocumentTag.LockContentControl property

عند ضبطه على`حقيقي` ، هذه الخاصية سوف تمنع المستخدم من حذف هذا**SDT** .

```csharp
public bool LockContentControl { get; set; }
```

## أمثلة

يوضح كيفية تطبيق قيود التحرير على علامات المستند المنظمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج علامة مستند منظمة ذات نص عادي، والتي تعمل كمربع نص يطالب المستخدم بملئه.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// قم بضبط خاصية "LockContents" على "true" لمنع المستخدم من تحرير محتويات مربع النص هذا.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// اضبط خاصية "LockContentControl" على "true" لمنع المستخدم من
// حذف علامة المستند المنظم هذه يدويًا في Microsoft Word.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### أنظر أيضا

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
