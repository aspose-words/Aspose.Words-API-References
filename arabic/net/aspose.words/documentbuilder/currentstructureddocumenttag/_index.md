---
title: DocumentBuilder.CurrentStructuredDocumentTag
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder ملكية. يحصل على علامة المستند المنظمة المحددة حاليًا في هذاDocumentBuilder .
type: docs
weight: 80
url: /ar/net/aspose.words/documentbuilder/currentstructureddocumenttag/
---
## DocumentBuilder.CurrentStructuredDocumentTag property

يحصل على علامة المستند المنظمة المحددة حاليًا في هذا[`DocumentBuilder`](../) .

```csharp
public StructuredDocumentTag CurrentStructuredDocumentTag { get; }
```

### أمثلة

يوضح كيفية تحريك مؤشر DocumentBuilder داخل علامة مستند منظمة.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// هناك عدة طرق لتحريك المؤشر:
// 1 - انتقل إلى الحرف الأول من علامة المستند المنظم حسب الفهرس.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - انتقل إلى الحرف الأول من علامة الوثيقة المنظمة حسب الكائن.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - انتقل إلى نهاية علامة المستند المنظمة الثانية.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);            

// احصل على علامة المستند المنظمة المحددة حاليًا.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### أنظر أيضا

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


