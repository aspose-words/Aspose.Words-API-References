---
title: DocumentBuilder.CurrentStory
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder ملكية. يحصل على القصة المحددة حاليًا في هذاDocumentBuilder .
type: docs
weight: 70
url: /ar/net/aspose.words/documentbuilder/currentstory/
---
## DocumentBuilder.CurrentStory property

يحصل على القصة المحددة حاليًا في هذا[`DocumentBuilder`](../) .

```csharp
public Story CurrentStory { get; }
```

### أمثلة

يوضح كيفية التعامل مع القصة الحالية لمنشئ المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// القصة هي نوع من العقد التي تحتوي على عقد فقرات فرعية، مثل النص الأساسي.
Assert.AreEqual(builder.CurrentStory, doc.FirstSection.Body);
Assert.AreEqual(builder.CurrentStory, builder.CurrentParagraph.ParentNode);
Assert.AreEqual(StoryType.MainText, builder.CurrentStory.StoryType);

builder.CurrentStory.AppendParagraph("Text added to current Story.");

// يمكن أن تحتوي القصة أيضًا على جداول.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndTable();

Assert.IsTrue(builder.CurrentStory.Tables.Contains(table));
```

### أنظر أيضا

* class [Story](../../story/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


