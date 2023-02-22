---
title: StructuredDocumentTag.LockContents
second_title: Aspose.Words لمراجع .NET API
description: StructuredDocumentTag ملكية. عند التعيين على صواب  ستمنع هذه الخاصية المستخدم من تحرير محتويات هذا المعاملة الخاصة والتفضيلية .
type: docs
weight: 200
url: /ar/net/aspose.words.markup/structureddocumenttag/lockcontents/
---
## StructuredDocumentTag.LockContents property

عند التعيين على "صواب" ، ستمنع هذه الخاصية المستخدم من تحرير محتويات هذا **المعاملة الخاصة والتفضيلية** .

```csharp
public bool LockContents { get; set; }
```

### أمثلة

يوضح كيفية تطبيق قيود التحرير على علامات المستند المنظمة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل علامة مستند منظم بنص عادي ، والذي يعمل كمربع نص يطالب المستخدم بتعبئته.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// اضبط خاصية "LockContents" على "true" لمنع المستخدم من تحرير محتويات مربع النص هذا.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// اضبط خاصية "LockContentControl" على "true" لمنع المستخدم من الدخول
// حذف علامة المستند المهيكلة يدويًا في Microsoft Word.
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


