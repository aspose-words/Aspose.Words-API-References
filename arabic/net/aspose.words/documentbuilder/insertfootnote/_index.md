---
title: DocumentBuilder.InsertFootnote
linktitle: InsertFootnote
articleTitle: InsertFootnote
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مستنداتك بسهولة باستخدام طريقة InsertFootnote في DocumentBuilder - قم بإضافة الحواشي السفلية أو النهائية بسهولة لتحقيق وضوح واحترافية أفضل.
type: docs
weight: 340
url: /ar/net/aspose.words/documentbuilder/insertfootnote/
---
## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string*) {#insertfootnote}

يقوم بإدراج حاشية سفلية أو تعليق ختامي في المستند.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| footnoteType | FootnoteType | يحدد ما إذا كان سيتم إدراج حاشية سفلية أو حاشية نهائية. |
| footnoteText | String | يحدد نص الحاشية السفلية. |

### قيمة الإرجاع

إرجاع كائن الحاشية السفلية الذي تم إنشاؤه للتو.

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

### أنظر أيضا

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string, string*) {#insertfootnote_1}

يقوم بإدراج حاشية سفلية أو تعليق ختامي في المستند.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText, string referenceMark)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| footnoteType | FootnoteType | يحدد ما إذا كان سيتم إدراج حاشية سفلية أو حاشية نهائية. |
| footnoteText | String | يحدد نص الحاشية السفلية. |
| referenceMark | String | يحدد علامة المرجع المخصصة للحاشية السفلية. |

### قيمة الإرجاع

إرجاع كائن الحاشية السفلية الذي تم إنشاؤه للتو.

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

### أنظر أيضا

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
