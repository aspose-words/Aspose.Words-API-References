---
title: HeaderFooter.ParentSection
second_title: Aspose.Words لمراجع .NET API
description: HeaderFooter ملكية. الحصول على القسم الأصل من هذه القصة .
type: docs
weight: 60
url: /ar/net/aspose.words/headerfooter/parentsection/
---
## HeaderFooter.ParentSection property

الحصول على القسم الأصل من هذه القصة .

```csharp
public Section ParentSection { get; }
```

### ملاحظات

**قسم الوالدين** يعادل`(القسم) ParentNode`.

### أمثلة

يوضح كيفية ربط الرؤوس والتذييلات بين الأقسام.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// الانتقال إلى القسم الأول وإنشاء رأس وتذييل. بشكل افتراضي،
// سيظهر الرأس والتذييل فقط على صفحات القسم الذي يحتوي عليهما.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// يمكننا ربط رؤوس / تذييلات القسم برؤوس / تذييلات القسم السابق
// للسماح لقسم الارتباط بعرض رؤوس / تذييلات القسم المرتبط.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// سيظل لكل قسم كائنات رأس / تذييل خاصة به. عندما نربط الأقسام ،
// سيعرض قسم الارتباط رأس / تذييلات القسم المرتبط مع الاحتفاظ به.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// ربط رؤوس / تذييلات القسم الثالث برؤوس / تذييلات القسم الثاني.
// يرتبط القسم الثاني بالفعل برأس / تذييلات القسم الأول ،
// لذلك سيؤدي الارتباط بالقسم الثاني إلى إنشاء سلسلة ارتباط.
// ستعرض الأقسام الأولى والثانية والثالثة رؤوس القسم الأول.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// يمكننا إلغاء ربط رأس / تذييلات القسم السابق بتمرير "خطأ" عند استدعاء طريقة LinkToPrevious.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// يمكننا أيضًا تحديد نوع معين فقط من الرأس / التذييل للربط باستخدام هذه الطريقة.
// سيكون للقسم الثالث الآن نفس تذييل القسمين الثاني والأول ، لكن ليس الرأس.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// لا يمكن لرأس / تذييلات القسم الأول ربط نفسها بأي شيء لأنه لا يوجد قسم سابق.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// كل رأس / تذييلات القسم الثاني مرتبطة برؤوس / تذييلات القسم الأول.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// في القسم الثالث ، يتم ربط التذييل فقط بتذييل القسم الأول عبر القسم الثاني.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### أنظر أيضا

* class [Section](../../section/)
* class [HeaderFooter](../)
* مساحة الاسم [Aspose.Words](../../headerfooter/)
* المجسم [Aspose.Words](../../../)


