---
title: FootnoteType Enum
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.FootnoteType enum. ميّز بسهولة بين الحواشي السفلية والختامية لتحسين تنسيق المستندات ووضوحها.
type: docs
weight: 5020
url: /ar/net/aspose.words.notes/footnotetype/
---
## FootnoteType enumeration

يحدد ما إذا كانت هذه حاشية سفلية أم حاشية ختامية.

```csharp
public enum FootnoteType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Footnote | `0` | الكائن عبارة عن حاشية سفلية. |
| Endnote | `1` | الكائن عبارة عن حاشية ختامية. |

## ملاحظات

يتم تمثيل كل من الحواشي السفلية والختامية بواسطة الكائنات بواسطةFootnote فئة . استخدم[`FootnoteType`](../footnote/footnotetype/) للتمييز بين الحواشي السفلية والحواشي النهائية.

## أمثلة

يوضح كيفية الإشارة إلى النص باستخدام الحاشية السفلية والحاشية الختامية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل بعض النص وقم بتمييزه بحاشية سفلية مع تعيين الخاصية IsAuto على "true" بشكل افتراضي،
// لذلك سيتم ترقيم العلامة الظاهرة في نص الموضوع تلقائيًا عند "1"،
//وسوف تظهر الحاشية السفلية في أسفل الصفحة.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// أدخل المزيد من النص وقم بتمييزه بملاحظة ختامية باستخدام علامة مرجعية مخصصة،
// والتي سيتم استخدامها بدلاً من الرقم "2" وتعيين "IsAuto" إلى false.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// تظهر الحواشي دائمًا في أسفل النص المرجعي الخاص بها،
// لذا فإن كسر هذه الصفحة لن يؤثر على الحاشية السفلية.
// من ناحية أخرى، تكون الحواشي الختامية دائمًا في نهاية المستند
// بحيث يؤدي كسر هذه الصفحة إلى دفع الحاشية السفلية إلى الصفحة التالية.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

يوضح كيفية إدراج الحواشي السفلية وتخصيصها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف نصًا، وأشر إليه بحاشية سفلية. ستُضيف هذه الحاشية إشارة علوية صغيرة.
// ضع علامة بعد النص الذي تشير إليه وقم بإنشاء إدخال أسفل نص الهيئة الرئيسي في أسفل الصفحة.
// سيحتوي هذا الإدخال على علامة مرجع الحاشية السفلية ونص المرجع،
// والتي سنمررها إلى طريقة "InsertFootnote" الخاصة بمنشئ المستندات.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// إذا تم تعيين هذه الخاصية على "true"، فسيتم استخدام علامة مرجع الحاشية السفلية لدينا
//سيكون فهرسها بين جميع حواشي القسم.
// هذه هي الحاشية الأولى، لذا فإن علامة المرجع ستكون "1".
Assert.True(footnote.IsAuto);

 // يمكننا نقل منشئ المستند داخل الحاشية السفلية لتحرير نص المرجع الخاص به.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// يمكننا تعيين علامة مرجعية مخصصة يستخدمها الحاشية السفلية بدلاً من رقم الفهرس الخاص بها.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// ستظل الإشارة المرجعية التي تم ضبط علم "IsAuto" عليها على "true" تعرض فهرسها الحقيقي
// حتى لو كانت الإشارات المرجعية السابقة تعرض علامات مرجعية مخصصة، فإن علامة مرجع هذه الإشارة المرجعية ستكون "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Notes](../../aspose.words.notes/)
* المجسم [Aspose.Words](../../)
