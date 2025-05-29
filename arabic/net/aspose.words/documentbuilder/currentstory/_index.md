---
title: DocumentBuilder.CurrentStory
linktitle: CurrentStory
articleTitle: CurrentStory
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية CurrentStory في DocumentBuilder للوصول إلى القصة المحددة وإدارتها بكفاءة، مما يعزز تجربة تحرير المستندات لديك.
type: docs
weight: 70
url: /ar/net/aspose.words/documentbuilder/currentstory/
---
## DocumentBuilder.CurrentStory property

يحصل على القصة المحددة حاليًا في هذه[`DocumentBuilder`](../) .

```csharp
public Story CurrentStory { get; }
```

## أمثلة

يوضح كيفية العمل مع القصة الحالية لمنشئ المستندات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// القصة هي نوع من العقد التي تحتوي على عقد فقرة فرعية، مثل النص.
Assert.AreEqual(builder.CurrentStory, doc.FirstSection.Body);
Assert.AreEqual(builder.CurrentStory, builder.CurrentParagraph.ParentNode);
Assert.AreEqual(StoryType.MainText, builder.CurrentStory.StoryType);

builder.CurrentStory.AppendParagraph("Text added to current Story.");

//يمكن أن تحتوي القصة أيضًا على جداول.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
