---
title: Story.StoryType
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية StoryType لتحديد قصصك وتصنيفها بسهولة، مما يعزز التنظيم ويحسن تجربة سرد القصص لديك.
type: docs
weight: 40
url: /ar/net/aspose.words/story/storytype/
---
## Story.StoryType property

يحصل على نوع هذه القصة.

```csharp
public StoryType StoryType { get; }
```

## أمثلة

يوضح كيفية إزالة كافة الأشكال من العقدة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم DocumentBuilder لإدراج شكل. هذا شكل مضمّن،
// والتي تحتوي على فقرة رئيسية، وهي عقدة فرعية لجسم القسم الأول.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

//يمكننا حذف جميع الأشكال من الفقرات الفرعية لهذا النص.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### أنظر أيضا

* enum [StoryType](../../storytype/)
* class [Story](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
