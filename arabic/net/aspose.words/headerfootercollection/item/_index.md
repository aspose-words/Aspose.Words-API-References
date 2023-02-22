---
title: HeaderFooterCollection.Item
second_title: Aspose.Words لمراجع .NET API
description: HeaderFooterCollection ملكية. يسترجع أ تذييل الرأس في الفهرس المحدد.
type: docs
weight: 10
url: /ar/net/aspose.words/headerfootercollection/item/
---
## HeaderFooterCollection indexer (1 of 2)

يسترجع أ **تذييل الرأس** في الفهرس المحدد.

```csharp
public HeaderFooter this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس في المجموعة. |

### ملاحظات

المؤشر على أساس الصفر.

يُسمح بالفهارس السلبية وتشير إلى الوصول من الجزء الخلفي من المجموعة. على سبيل المثال -1 تعني العنصر الأخير ، -2 تعني العنصر الثاني قبل الأخير وهكذا.

إذا كان الفهرس أكبر من أو يساوي عدد العناصر في القائمة ، فسيُرجع هذا مرجعًا فارغًا.

إذا كان الفهرس سالبًا وكانت قيمته المطلقة أكبر من عدد العناصر في القائمة ، فسيُرجع هذا مرجعًا فارغًا.

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

* class [HeaderFooter](../../headerfooter/)
* class [HeaderFooterCollection](../)
* مساحة الاسم [Aspose.Words](../../headerfootercollection/)
* المجسم [Aspose.Words](../../../)

---

## HeaderFooterCollection indexer (2 of 2)

يسترجع أ **تذييل الرأس** من النوع المحدد.

```csharp
public HeaderFooter this[HeaderFooterType headerFooterType] { get; }
```

| معامل | وصف |
| --- | --- |
| headerFooterType | أ[`HeaderFooterType`](../../headerfootertype/) value التي تحدد نوع الرأس / التذييل المطلوب استرداده. |

### ملاحظات

يتم إرجاع القيمة فارغة إذا لم يتم العثور على رأس / تذييل الصفحة من النوع المحدد.

### أمثلة

يوضح كيفية استبدال النص في تذييل المستند.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

يوضح كيفية حذف كل التذييلات من مستند.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// كرر خلال كل قسم وقم بإزالة التذييلات من كل نوع.
foreach (Section section in doc.OfType<Section>())
{
    // هناك ثلاثة أنواع من أنواع التذييل والرأس.
    // 1 - الرأس / التذييل "الأول" ، والذي يظهر فقط في الصفحة الأولى من القسم.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - الرأس / التذييل "الأساسي" ، والذي يظهر في الصفحات الفردية.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - رأس / تذييل "زوجي" ، والذي يظهر في الصفحات الزوجية.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

### أنظر أيضا

* class [HeaderFooter](../../headerfooter/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooterCollection](../)
* مساحة الاسم [Aspose.Words](../../headerfootercollection/)
* المجسم [Aspose.Words](../../../)


