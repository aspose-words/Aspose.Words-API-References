---
title: DocumentBuilder.MoveToStructuredDocumentTag
linktitle: MoveToStructuredDocumentTag
articleTitle: MoveToStructuredDocumentTag
second_title: Aspose.Words لـ .NET
description: DocumentBuilder MoveToStructuredDocumentTag طريقة. ينقل المؤشر إلى علامة مستند منظمة في القسم الحالي في C#.
type: docs
weight: 580
url: /ar/net/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## MoveToStructuredDocumentTag(*int, int*) {#movetostructureddocumenttag_1}

ينقل المؤشر إلى علامة مستند منظمة في القسم الحالي.

```csharp
public void MoveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| structuredDocumentTagIndex | Int32 | فهرس علامة الوثيقة المنظمة للانتقال إليها. |
| characterIndex | Int32 | فهرس الحرف الموجود داخل علامة المستند المنظم. تتيح لك القيمة السالبة تحديد موضع من نهاية علامة المستند المنظم. استخدم -1 to للانتقال إلى نهاية علامة المستند المنظمة. إذا كانت علامة المستند المنظم على مستوى الكتلة، وكنت تريد نقل المؤشر إلى نهاية الفقرة الأخيرة، فحدد -2. |

## ملاحظات

يتم التنقل داخل القصة الحالية للقسم الحالي. أي أنه إذا قمت بنقل المؤشر إلى الرأس الأساسي للقسم الأول، إذن*structuredDocumentTagIndex*حدد فهرس علامة المستند المنظم داخل رأس هذا القسم.

متى*structuredDocumentTagIndex* أكبر من أو يساوي 0، فإنه يحدد مؤشر من بداية القسم حيث يكون 0 أول علامة مستند منظمة. متى *structuredDocumentTagIndex* أقل من 0، فقد حددت فهرسًا من نهاية القسم مع كون -1 آخر علامة مستند منظمة.

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

---

## MoveToStructuredDocumentTag(*[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), int*) {#movetostructureddocumenttag}

يحرك المؤشر إلى علامة الوثيقة المنظمة.

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | علامة الوثيقة المنظمة للانتقال إليها. |
| characterIndex | Int32 | فهرس الحرف الموجود داخل علامة المستند المنظم. تتيح لك القيمة السالبة تحديد موضع من نهاية علامة المستند المنظم. استخدم -1 to للانتقال إلى نهاية علامة المستند المنظمة. إذا كانت علامة المستند المنظم على مستوى الكتلة، وكنت تريد نقل المؤشر إلى نهاية الفقرة الأخيرة، فحدد -2. |

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

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
