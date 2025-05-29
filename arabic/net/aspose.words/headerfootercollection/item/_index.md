---
title: HeaderFooterCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: الوصول إلى رؤوس وتذييلات الصفحات بسهولة باستخدام خاصية العنصر. استرجع رؤوسًا وتذييلات محددة باستخدام الفهرس لإدارة مستنداتك بشكل مبسط.
type: docs
weight: 10
url: /ar/net/aspose.words/headerfootercollection/item/
---
## HeaderFooterCollection indexer (1 of 2)

يسترجع[`HeaderFooter`](../../headerfooter/) عند الفهرس المعطى.

```csharp
public HeaderFooter this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس للمجموعة. |

## ملاحظات

المؤشر يعتمد على الصفر.

يُسمح بالمؤشرات السلبية وتشير إلى الوصول من الجزء الخلفي للمجموعة. على سبيل المثال، -1 يعني العنصر الأخير، -2 يعني العنصر الثاني قبل الأخير وهكذا.

إذا كان الفهرس أكبر من أو يساوي عدد العناصر في القائمة، فسوف يؤدي هذا إلى إرجاع مرجع فارغ.

إذا كان الفهرس سلبيًا وكانت قيمته المطلقة أكبر من عدد العناصر في القائمة، فسيؤدي هذا إلى إرجاع مرجع فارغ.

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

* class [HeaderFooter](../../headerfooter/)
* class [HeaderFooterCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## HeaderFooterCollection indexer (2 of 2)

يسترجع[`HeaderFooter`](../../headerfooter/) من النوع المحدد.

```csharp
public HeaderFooter this[HeaderFooterType headerFooterType] { get; }
```

| معامل | وصف |
| --- | --- |
| headerFooterType | أ[`HeaderFooterType`](../../headerfootertype/) value التي تحدد نوع الرأس/التذييل الذي سيتم استرداده. |

## ملاحظات

إرجاع`باطل`إذا لم يتم العثور على رأس/تذييل النوع المحدد.

## أمثلة

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

يوضح كيفية حذف كافة التذييلات من المستند.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// قم بالتكرار خلال كل قسم وإزالة التذييلات من كل نوع.
foreach (Section section in doc.OfType<Section>())
{
    // هناك ثلاثة أنواع من أنواع التذييل والرأس.
    // 1 - "الرأس/التذييل الأول"، والذي يظهر فقط في الصفحة الأولى من القسم.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - الرأس/التذييل "الأساسي"، والذي يظهر في الصفحات الفردية.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - رأس/تذييل "الزوجي"، والذي يظهر في الصفحات الزوجية.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
