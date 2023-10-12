---
title: Class HeaderFooterCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.HeaderFooterCollection فصل. يوفر الوصول المكتوب إلىHeaderFooter العقد أSection .
type: docs
weight: 3110
url: /ar/net/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class

يوفر الوصول المكتوب إلى[`HeaderFooter`](../headerfooter/) العقد أ[`Section`](../section/) .

لمعرفة المزيد، قم بزيارة[العمل مع الرؤوس والتذييلات](https://docs.aspose.com/words/net/working-with-headers-and-footers/) مقالة توثيقية.

```csharp
public class HeaderFooterCollection : NodeCollection
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | الحصول على عدد العقد في المجموعة. |
| [Item](../../aspose.words/headerfootercollection/item/) { get; } | يسترد أ[`HeaderFooter`](../headerfooter/) في الفهرس المحدد. (3 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | إضافة عقدة إلى نهاية المجموعة. |
| [Clear](../../aspose.words/nodecollection/clear/)() | إزالة كافة العقد من هذه المجموعة ومن المستند. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | تحديد ما إذا كانت العقدة موجودة في المجموعة. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | يوفر تكرارًا بسيطًا لنمط "foreach" عبر مجموعة العقد. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | إرجاع الفهرس الصفري للعقدة المحددة. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | إدراج عقدة في المجموعة في الفهرس المحدد. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious_1)(bool) | ربط أو إلغاء ربط جميع الرؤوس والتذييلات بالرؤوس والتذييلات المقابلة لها في القسم السابق. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious)(HeaderFooterType, bool) | ربط أو إلغاء ربط الرأس أو التذييل المحدد بالرأس أو التذييل المقابل في القسم السابق. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | إزالة العقدة من المجموعة ومن المستند. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | إزالة العقدة الموجودة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](../../aspose.words/headerfootercollection/toarray/#toarray)() | نسخ الكل`HeaderForter` من المجموعة إلى مجموعة جديدة من`HeaderForter` ق. (2 methods) |

### ملاحظات

يمكن أن يكون هناك حد أقصى واحد[`HeaderFooter`](../headerfooter/)

لكل واحد[`HeaderFooterType`](../headerfootertype/) لكل [`Section`](../section/) .

[`HeaderFooter`](../headerfooter/) يمكن أن تظهر الكائنات بأي ترتيب في المجموعة.

### أمثلة

يوضح كيفية حذف جميع التذييلات من المستند.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// كرر كل قسم وقم بإزالة التذييلات من كل نوع.
foreach (Section section in doc.OfType<Section>())
{
    // هناك ثلاثة أنواع من أنواع التذييل والرأس.
    // 1 - الرأس/التذييل "الأول"، والذي يظهر فقط في الصفحة الأولى من القسم.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - الرأس/التذييل "الأساسي"، الذي يظهر على الصفحات الفردية.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - الرأس/التذييل "الزوجي"، الذي يظهر في الصفحات الزوجية.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

يوضح كيفية إنشاء رأس وتذييل.

```csharp
Document doc = new Document();

// قم بإنشاء رأس وألحق فقرة به. النص في تلك الفقرة
// سيظهر في أعلى كل صفحة من هذا القسم، فوق النص الأساسي.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// قم بإنشاء تذييل وإلحاق فقرة به. النص في تلك الفقرة
// سيظهر في أسفل كل صفحة من هذا القسم، أسفل النص الرئيسي.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### أنظر أيضا

* class [NodeCollection](../nodecollection/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


