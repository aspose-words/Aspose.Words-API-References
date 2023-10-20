---
title: FootnoteType Enum
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Notes.FootnoteType تعداد. يحدد ما إذا كانت هذه حاشية سفلية أم تعليق ختامي في C#.
type: docs
weight: 4300
url: /ar/net/aspose.words.notes/footnotetype/
---
## FootnoteType enumeration

يحدد ما إذا كانت هذه حاشية سفلية أم تعليق ختامي.

```csharp
public enum FootnoteType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Footnote | `0` | الكائن عبارة عن حاشية سفلية. |
| Endnote | `1` | الكائن عبارة عن تعليق ختامي. |

## ملاحظات

يتم تمثيل كل من الحواشي السفلية والتعليقات الختامية بكائنات بواسطةFootnote فئة. يستخدم[`FootnoteType`](../footnote/footnotetype/) للتمييز بين الحواشي السفلية والتعليقات الختامية.

## أمثلة

يوضح كيفية الإشارة إلى النص باستخدام حاشية سفلية وتعليق ختامي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج بعض النص ووضع علامة عليه باستخدام حاشية سفلية مع تعيين الخاصية IsAuto على "صحيح" افتراضيًا،
// لذلك سيتم ترقيم العلامة الموجودة في النص الأساسي تلقائيًا عند "1"،
// وستظهر الحاشية السفلية في أسفل الصفحة.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// قم بإدراج المزيد من النص ووضع علامة عليه بتعليق ختامي بعلامة مرجعية مخصصة،
// والذي سيتم استخدامه بدلاً من الرقم "2" وضبط "IsAuto" على "خطأ".
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// تظهر الحواشي السفلية دائمًا أسفل النص المشار إليه،
// لذلك لن يؤثر فاصل الصفحات هذا على الحاشية السفلية.
// ومن ناحية أخرى، تكون التعليقات الختامية دائمًا في نهاية المستند
// بحيث يؤدي فاصل الصفحة هذا إلى دفع التعليق الختامي إلى الصفحة التالية.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

يوضح كيفية إدراج الحواشي السفلية وتخصيصها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف نصًا، وأشر إليه بحاشية سفلية. ستضع هذه الحاشية السفلية مرجعًا مرتفعًا صغيرًا
// ضع علامة بعد النص الذي تشير إليه وقم بإنشاء إدخال أسفل النص الأساسي في أسفل الصفحة.
// سيحتوي هذا الإدخال على العلامة المرجعية للحاشية السفلية والنص المرجعي،
// والذي سنمرره إلى طريقة "InsertFootnote" الخاصة بمنشئ المستندات.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// إذا تم تعيين هذه الخاصية على "صحيح"، فستكون العلامة المرجعية للحاشية السفلية
// سيكون فهرسه بين جميع الحواشي السفلية للقسم.
// هذه هي الحاشية السفلية الأولى، لذا ستكون العلامة المرجعية "1".
Assert.True(footnote.IsAuto);

 // يمكننا نقل أداة إنشاء المستندات داخل الحاشية السفلية لتحرير النص المرجعي الخاص بها.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// يمكننا تعيين علامة مرجعية مخصصة تستخدمها الحاشية السفلية بدلاً من رقم الفهرس الخاص بها.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// الإشارة المرجعية التي تم ضبط علامة "IsAuto" على "صحيح" ستظل تُظهر فهرسها الحقيقي
// حتى لو كانت الإشارات المرجعية السابقة تعرض علامات مرجعية مخصصة، فستكون العلامة المرجعية لهذه الإشارة المرجعية "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Notes](../../aspose.words.notes/)
* المجسم [Aspose.Words](../../)
