---
title: DocumentBuilder.IsAtEndOfStructuredDocumentTag
linktitle: IsAtEndOfStructuredDocumentTag
articleTitle: IsAtEndOfStructuredDocumentTag
second_title: Aspose.Words لـ .NET
description: DocumentBuilder IsAtEndOfStructuredDocumentTag ملكية. إرجاعحقيقي إذا كان المؤشر في نهاية علامة مستند منظم في C#.
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

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
