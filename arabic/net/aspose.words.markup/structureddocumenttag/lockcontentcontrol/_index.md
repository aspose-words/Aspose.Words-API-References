---
title: StructuredDocumentTag.LockContentControl
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTag ملكية. عند الضبط علىحقيقي  ستمنع هذه الخاصية المستخدم من حذف هذا المعاملة الخاصة والتفضيلية .
type: docs
weight: 190
url: /ar/net/aspose.words.markup/structureddocumenttag/lockcontentcontrol/
---
## StructuredDocumentTag.LockContentControl property

عند الضبط على`حقيقي` ، ستمنع هذه الخاصية المستخدم من حذف هذا **المعاملة الخاصة والتفضيلية** .

```csharp
public bool LockContentControl { get; set; }
```

### أمثلة

يوضح كيفية تطبيق قيود التحرير على علامات المستندات المنظمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج علامة مستند منظمة ذات نص عادي، والتي تعمل كمربع نص يطالب المستخدم بملءها.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// اضبط خاصية "LockContents" على "true" لمنع المستخدم من تحرير محتويات مربع النص هذا.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// اضبط خاصية "LockContentControl" على "صحيح" لمنع المستخدم منها
// حذف علامة المستند المنظمة يدويًا في Microsoft Word.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### أنظر أيضا

* class [StructuredDocumentTag](../)
* مساحة الاسم [Aspose.Words.Markup](../../structureddocumenttag/)
* المجسم [Aspose.Words](../../../)


