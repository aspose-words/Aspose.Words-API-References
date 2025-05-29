---
title: HeaderFooterCollection.LinkToPrevious
linktitle: LinkToPrevious
articleTitle: LinkToPrevious
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة LinkToPrevious في HeaderFooterCollection لتوصيل أو فصل الرؤوس والتذييلات بسهولة عبر أقسام المستند للحصول على تنسيق سلس.
type: docs
weight: 20
url: /ar/net/aspose.words/headerfootercollection/linktoprevious/
---
## LinkToPrevious(*bool*) {#linktoprevious_1}

يربط أو يلغي ربط جميع الرؤوس والتذييلات بالرؤوس والتذييلات المقابلة لها في القسم السابق.

```csharp
public void LinkToPrevious(bool isLinkToPrevious)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| isLinkToPrevious | Boolean | `حقيقي` لربط الرؤوس والتذييلات بالقسم السابق؛ `خطأ شنيع` لفك ارتباطهم. |

## ملاحظات

إذا لم يكن أي من الرؤوس أو التذييلات موجودًا، فسيتم إنشائها تلقائيًا.

## أمثلة

يوضح كيفية ربط الرؤوس والتذييلات بين الأقسام.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// انتقل إلى القسم الأول وأنشئ رأسًا وتذييلًا. افتراضيًا،
// سوف يظهر الرأس والتذييل فقط في الصفحات الموجودة في القسم الذي يحتوي عليهما.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// يمكننا ربط رؤوس/تذييلات القسم برؤوس/تذييلات القسم السابق
// للسماح لقسم الارتباط بعرض رؤوس/تذييلات القسم المرتبط.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// سيظل لكل قسم كائنات رأس/تذييل خاصة به. عند ربط الأقسام،
// سيعرض القسم المرتبط رأس/تذييل القسم المرتبط مع الاحتفاظ برأس/تذييل القسم الخاص به.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// ربط رؤوس/تذييلات القسم الثالث برؤوس/تذييلات القسم الثاني.
// يرتبط القسم الثاني بالفعل برأس/تذييلات القسم الأول،
// لذا فإن الارتباط بالقسم الثاني سيؤدي إلى إنشاء سلسلة ارتباط.
// سيتم عرض عناوين القسم الأول، والثاني، والآن القسم الثالث.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// يمكننا إلغاء ربط رأس/تذييل القسم السابق عن طريق تمرير "false" عند استدعاء طريقة LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

//يمكننا أيضًا تحديد نوع معين فقط من الرأس/التذييل للربط باستخدام هذه الطريقة.
// الآن سيكون للقسم الثالث نفس التذييل مثل القسمين الثاني والأول، ولكن ليس الرأس.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// لا يمكن لرأس/تذييل القسم الأول ربط نفسه بأي شيء لأنه لا يوجد قسم سابق.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// ترتبط جميع رؤوس/تذييلات القسم الثاني برؤوس/تذييلات القسم الأول.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// في القسم الثالث، يتم ربط التذييل فقط بتذييل القسم الأول عبر القسم الثاني.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### أنظر أيضا

* class [HeaderFooterCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## LinkToPrevious(*[HeaderFooterType](../../headerfootertype/), bool*) {#linktoprevious}

يربط أو يلغي ربط الرأس أو التذييل المحدد بالرأس أو التذييل المقابل في القسم السابق.

```csharp
public void LinkToPrevious(HeaderFooterType headerFooterType, bool isLinkToPrevious)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | أ[`HeaderFooterType`](../../headerfootertype/) value التي تحدد الرأس أو التذييل الذي سيتم ربطه/إلغاء ربطه. |
| isLinkToPrevious | Boolean | `حقيقي` لربط الرأس أو التذييل بالقسم السابق؛ `خطأ شنيع` لإلغاء الارتباط. |

## ملاحظات

إذا لم يكن الرأس أو التذييل للنوع المحدد موجودًا، فسيتم إنشائه تلقائيًا.

## أمثلة

يوضح كيفية ربط الرؤوس والتذييلات بين الأقسام.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// انتقل إلى القسم الأول وأنشئ رأسًا وتذييلًا. افتراضيًا،
// سوف يظهر الرأس والتذييل فقط في الصفحات الموجودة في القسم الذي يحتوي عليهما.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// يمكننا ربط رؤوس/تذييلات القسم برؤوس/تذييلات القسم السابق
// للسماح لقسم الارتباط بعرض رؤوس/تذييلات القسم المرتبط.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// سيظل لكل قسم كائنات رأس/تذييل خاصة به. عند ربط الأقسام،
// سيعرض القسم المرتبط رأس/تذييل القسم المرتبط مع الاحتفاظ برأس/تذييل القسم الخاص به.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// ربط رؤوس/تذييلات القسم الثالث برؤوس/تذييلات القسم الثاني.
// يرتبط القسم الثاني بالفعل برأس/تذييلات القسم الأول،
// لذا فإن الارتباط بالقسم الثاني سيؤدي إلى إنشاء سلسلة ارتباط.
// سيتم عرض عناوين القسم الأول، والثاني، والآن القسم الثالث.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// يمكننا إلغاء ربط رأس/تذييل القسم السابق عن طريق تمرير "false" عند استدعاء طريقة LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

//يمكننا أيضًا تحديد نوع معين فقط من الرأس/التذييل للربط باستخدام هذه الطريقة.
// الآن سيكون للقسم الثالث نفس التذييل مثل القسمين الثاني والأول، ولكن ليس الرأس.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// لا يمكن لرأس/تذييل القسم الأول ربط نفسه بأي شيء لأنه لا يوجد قسم سابق.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// ترتبط جميع رؤوس/تذييلات القسم الثاني برؤوس/تذييلات القسم الأول.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// في القسم الثالث، يتم ربط التذييل فقط بتذييل القسم الأول عبر القسم الثاني.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### أنظر أيضا

* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooterCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
