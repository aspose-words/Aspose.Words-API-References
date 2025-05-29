---
title: DocumentBuilder.MoveToStructuredDocumentTag
linktitle: MoveToStructuredDocumentTag
articleTitle: MoveToStructuredDocumentTag
second_title: Aspose.Words لـ .NET
description: انتقل بسهولة إلى علامات المستندات المنظمة باستخدام طريقة MoveToStructuredDocumentTag في DocumentBuilder، مما يعزز كفاءة تحرير المستندات لديك.
type: docs
weight: 620
url: /ar/net/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## MoveToStructuredDocumentTag(*int, int*) {#movetostructureddocumenttag_1}

يحرك المؤشر إلى علامة مستند منظمة في القسم الحالي.

```csharp
public void MoveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| structuredDocumentTagIndex | Int32 | فهرس علامة المستند المنظم الذي سيتم الانتقال إليه. |
| characterIndex | Int32 | فهرس الحرف داخل وسم المستند المنظم. . تتيح لك القيمة السالبة تحديد موضع من نهاية وسم المستند المنظم. استخدم -1 للانتقال إلى نهاية وسم المستند المنظم. إذا كان وسم المستند المنظم على مستوى الكتلة، وكنت ترغب في نقل المؤشر إلى نهاية فقرته الأخيرة، فحدد -2. |

## ملاحظات

يتم التنقل داخل القصة الحالية للقسم الحالي. أي، إذا نقلتَ مؤشر x000d_ إلى العنوان الرئيسي للقسم الأول،*structuredDocumentTagIndex* قام بتحديد فهرس علامة المستند المنظم داخل رأس هذا القسم.

متى*structuredDocumentTagIndex* عندما يكون أكبر من أو يساوي 0، فإنه يحدد index من بداية القسم، حيث يكون 0 هو أول علامة مستند منظمة. When *structuredDocumentTagIndex*أقل من 0، فقد حدد فهرسًا من نهاية قسم مع كون -1 هو علامة المستند المنظم الأخيرة.

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

---

## MoveToStructuredDocumentTag(*[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), int*) {#movetostructureddocumenttag}

يحرك المؤشر إلى علامة المستند المنظم.

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | علامة المستند المنظم الذي سيتم الانتقال إليه. |
| characterIndex | Int32 | فهرس الحرف داخل وسم المستند المنظم. . تتيح لك القيمة السالبة تحديد موضع من نهاية وسم المستند المنظم. استخدم -1 للانتقال إلى نهاية وسم المستند المنظم. إذا كان وسم المستند المنظم على مستوى الكتلة، وكنت ترغب في نقل المؤشر إلى نهاية فقرته الأخيرة، فحدد -2. |

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
