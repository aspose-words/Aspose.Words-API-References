---
title: DocumentBuilder.InsertFootnote
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. إدراج حاشية سفلية أو تعليق ختامي في المستند.
type: docs
weight: 340
url: /ar/net/aspose.words/documentbuilder/insertfootnote/
---
## InsertFootnote(FootnoteType, string) {#insertfootnote}

إدراج حاشية سفلية أو تعليق ختامي في المستند.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| footnoteType | FootnoteType | يحدد ما إذا كان سيتم إدراج حاشية سفلية أو تعليق ختامي. |
| footnoteText | String | يحدد نص الحاشية السفلية. |

### قيمة الإرجاع

إرجاع كائن الحاشية السفلية الذي تم إنشاؤه للتو.

### أمثلة

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

### أنظر أيضا

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertFootnote(FootnoteType, string, string) {#insertfootnote_1}

إدراج حاشية سفلية أو تعليق ختامي في المستند.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText, string referenceMark)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| footnoteType | FootnoteType | يحدد ما إذا كان سيتم إدراج حاشية سفلية أو تعليق ختامي. |
| footnoteText | String | يحدد نص الحاشية السفلية. |
| referenceMark | String | يحدد العلامة المرجعية المخصصة للحاشية السفلية. |

### قيمة الإرجاع

إرجاع كائن الحاشية السفلية الذي تم إنشاؤه للتو.

### أمثلة

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

### أنظر أيضا

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


