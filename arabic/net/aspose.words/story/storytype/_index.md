---
title: Story.StoryType
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words لـ .NET
description: Story StoryType ملكية. احصل على نوع هذه القصة في C#.
type: docs
weight: 40
url: /ar/net/aspose.words/story/storytype/
---
## Story.StoryType property

احصل على نوع هذه القصة.

```csharp
public StoryType StoryType { get; }
```

## أمثلة

يوضح كيفية إزالة كافة الأشكال من العقدة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم DocumentBuilder لإدراج شكل. وهذا شكل خطي
// التي تحتوي على فقرة أصل، وهي عقدة فرعية لنص القسم الأول.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// يمكننا حذف جميع الأشكال من الفقرات الفرعية لهذا الجسم.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### أنظر أيضا

* enum [StoryType](../../storytype/)
* class [Story](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
