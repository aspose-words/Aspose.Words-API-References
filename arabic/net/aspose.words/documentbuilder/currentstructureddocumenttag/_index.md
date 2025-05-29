---
title: DocumentBuilder.CurrentStructuredDocumentTag
linktitle: CurrentStructuredDocumentTag
articleTitle: CurrentStructuredDocumentTag
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية CurrentStructuredDocumentTag في DocumentBuilder. تمكّن من الوصول بسهولة إلى وسم المستند الهيكلي المحدد لإدارة مستندات فعّالة.
type: docs
weight: 80
url: /ar/net/aspose.words/documentbuilder/currentstructureddocumenttag/
---
## DocumentBuilder.CurrentStructuredDocumentTag property

يحصل على علامة المستند المنظمة المحددة حاليًا في هذا[`DocumentBuilder`](../) .

```csharp
public StructuredDocumentTag CurrentStructuredDocumentTag { get; }
```

## أمثلة

يوضح كيفية نقل مؤشر DocumentBuilder داخل علامة مستند منظمة.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// هناك عدة طرق لتحريك المؤشر:
// 1 - الانتقال إلى أول حرف من علامة المستند المنظم بواسطة الفهرس.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - الانتقال إلى أول حرف من علامة المستند المنظم بواسطة الكائن.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - الانتقال إلى نهاية علامة المستند المنظم الثانية.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);

// احصل على علامة المستند المنظم المحددة حاليًا.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### أنظر أيضا

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
