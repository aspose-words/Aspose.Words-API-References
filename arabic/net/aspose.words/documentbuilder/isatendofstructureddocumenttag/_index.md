---
title: DocumentBuilder.IsAtEndOfStructuredDocumentTag
linktitle: IsAtEndOfStructuredDocumentTag
articleTitle: IsAtEndOfStructuredDocumentTag
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IsAtEndOfStructuredDocumentTag في DocumentBuilder—تحقق مما إذا كان المؤشر موجودًا في نهاية علامة مستند منظمة لتحرير فعال!
type: docs
weight: 120
url: /ar/net/aspose.words/documentbuilder/isatendofstructureddocumenttag/
---
## DocumentBuilder.IsAtEndOfStructuredDocumentTag property

إرجاع**حقيقي** إذا كان المؤشر في نهاية علامة مستند منظم.

```csharp
public bool IsAtEndOfStructuredDocumentTag { get; }
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

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
