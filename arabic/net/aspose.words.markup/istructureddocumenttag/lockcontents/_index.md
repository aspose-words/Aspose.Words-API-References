---
title: IStructuredDocumentTag.LockContents
linktitle: LockContents
articleTitle: LockContents
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية قفل محتويات IStructuredDocumentTag أمان المستندات من خلال منع تعديلها. تأكد من سلامة ملف SDT الخاص بك!
type: docs
weight: 80
url: /ar/net/aspose.words.markup/istructureddocumenttag/lockcontents/
---
## IStructuredDocumentTag.LockContents property

عند تعيينها على true، ستمنع هذه الخاصية المستخدم من تحرير محتويات هذه**SDT** .

```csharp
public bool LockContents { get; set; }
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

* interface [IStructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
