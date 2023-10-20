---
title: HeaderFooterCollection.LinkToPrevious
linktitle: LinkToPrevious
articleTitle: LinkToPrevious
second_title: Aspose.Words لـ .NET
description: HeaderFooterCollection LinkToPrevious طريقة. ربط أو إلغاء ربط جميع الرؤوس والتذييلات بالرؤوس والتذييلات المقابلة لها في القسم السابق في C#.
type: docs
weight: 20
url: /ar/net/aspose.words/headerfootercollection/linktoprevious/
---
## LinkToPrevious(*bool*) {#linktoprevious_1}

ربط أو إلغاء ربط جميع الرؤوس والتذييلات بالرؤوس والتذييلات المقابلة لها في القسم السابق.

```csharp
public void LinkToPrevious(bool isLinkToPrevious)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| isLinkToPrevious | Boolean | `حقيقي` لربط الرؤوس والتذييلات بالقسم السابق؛ `خطأ شنيع` لفك الارتباط بينهما. |

## ملاحظات

في حالة عدم وجود أي من الرؤوس أو التذييلات، قم بإنشائها تلقائيًا.

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

// انتقل إلى القسم الأول وقم بإنشاء رأس وتذييل. بشكل افتراضي،
// لن يظهر الرأس والتذييل إلا على الصفحات الموجودة في القسم الذي يحتوي عليهما.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// يمكننا ربط رؤوس/تذييلات القسم برؤوس/تذييلات القسم السابق
// للسماح لقسم الارتباط بعرض رؤوس/تذييلات القسم المرتبط.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// سيظل لكل قسم كائنات الرأس/التذييل الخاصة به. عندما نربط الأقسام
// سيعرض قسم الارتباط رأس/تذييلات القسم المرتبط مع الاحتفاظ به.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// اربط رؤوس/تذييلات القسم الثالث برؤوس/تذييلات القسم الثاني.
// يرتبط القسم الثاني بالفعل برأس/تذييلات القسم الأول،
// لذا فإن الارتباط بالقسم الثاني سيؤدي إلى إنشاء سلسلة ارتباط.
// ستعرض الأقسام الأول والثاني والآن الثالث رؤوس القسم الأول.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// يمكننا إلغاء ربط رأس/تذييلات القسم السابق عن طريق تمرير "خطأ" عند استدعاء الأسلوب LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// يمكننا أيضًا تحديد نوع معين فقط من الرأس/التذييل للربط باستخدام هذه الطريقة.
// سيكون للقسم الثالث الآن نفس التذييل مثل القسمين الثاني والأول، ولكن ليس الرأس.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// لا يمكن لرأس/تذييلات القسم الأول ربط نفسها بأي شيء لأنه لا يوجد قسم سابق.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// جميع رؤوس/تذييلات القسم الثاني مرتبطة برؤوس/تذييلات القسم الأول.
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

ربط أو إلغاء ربط الرأس أو التذييل المحدد بالرأس أو التذييل المقابل في القسم السابق.

```csharp
public void LinkToPrevious(HeaderFooterType headerFooterType, bool isLinkToPrevious)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | أ[`HeaderFooterType`](../../headerfootertype/) value الذي يحدد الرأس أو التذييل للربط/إلغاء الارتباط. |
| isLinkToPrevious | Boolean | `حقيقي`لربط الرأس أو التذييل بالقسم السابق؛ `خطأ شنيع` لإلغاء الارتباط. |

## ملاحظات

في حالة عدم وجود رأس أو تذييل من النوع المحدد، قم بإنشائه تلقائيًا.

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

// انتقل إلى القسم الأول وقم بإنشاء رأس وتذييل. بشكل افتراضي،
// لن يظهر الرأس والتذييل إلا على الصفحات الموجودة في القسم الذي يحتوي عليهما.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// يمكننا ربط رؤوس/تذييلات القسم برؤوس/تذييلات القسم السابق
// للسماح لقسم الارتباط بعرض رؤوس/تذييلات القسم المرتبط.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// سيظل لكل قسم كائنات الرأس/التذييل الخاصة به. عندما نربط الأقسام
// سيعرض قسم الارتباط رأس/تذييلات القسم المرتبط مع الاحتفاظ به.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// اربط رؤوس/تذييلات القسم الثالث برؤوس/تذييلات القسم الثاني.
// يرتبط القسم الثاني بالفعل برأس/تذييلات القسم الأول،
// لذا فإن الارتباط بالقسم الثاني سيؤدي إلى إنشاء سلسلة ارتباط.
// ستعرض الأقسام الأول والثاني والآن الثالث رؤوس القسم الأول.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// يمكننا إلغاء ربط رأس/تذييلات القسم السابق عن طريق تمرير "خطأ" عند استدعاء الأسلوب LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// يمكننا أيضًا تحديد نوع معين فقط من الرأس/التذييل للربط باستخدام هذه الطريقة.
// سيكون للقسم الثالث الآن نفس التذييل مثل القسمين الثاني والأول، ولكن ليس الرأس.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// لا يمكن لرأس/تذييلات القسم الأول ربط نفسها بأي شيء لأنه لا يوجد قسم سابق.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// جميع رؤوس/تذييلات القسم الثاني مرتبطة برؤوس/تذييلات القسم الأول.
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
