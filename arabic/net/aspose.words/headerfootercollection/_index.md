---
title: HeaderFooterCollection Class
linktitle: HeaderFooterCollection
articleTitle: HeaderFooterCollection
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.HeaderFooterCollection للوصول بسهولة وكتابة إلى عقد Section HeaderFooter، مما يسهل إدارة المستندات ويعزز سير عملك.
type: docs
weight: 3540
url: /ar/net/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class

يوفر الوصول المكتوب إلى[`HeaderFooter`](../headerfooter/) عقدة من[`Section`](../section/) .

لمعرفة المزيد، قم بزيارة[العمل مع الرؤوس والتذييلات](https://docs.aspose.com/words/net/working-with-headers-and-footers/) مقالة توثيقية.

```csharp
public class HeaderFooterCollection : NodeCollection
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | يحصل على عدد العقد في المجموعة. |
| [Item](../../aspose.words/headerfootercollection/item/) { get; } | يسترجع[`HeaderFooter`](../headerfooter/) عند الفهرس المعطى. (3 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | يضيف عقدة إلى نهاية المجموعة. |
| [Clear](../../aspose.words/nodecollection/clear/)() | يزيل جميع العقد من هذه المجموعة ومن المستند. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | يحدد ما إذا كانت العقدة موجودة في المجموعة. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | يوفر تكرارًا بسيطًا بأسلوب "foreach" عبر مجموعة العقد. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | يعيد الفهرس المبني على الصفر للعقدة المحددة. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | يقوم بإدراج عقدة في المجموعة عند الفهرس المحدد. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious_1)(*bool*) | يربط أو يلغي ربط جميع الرؤوس والتذييلات بالرؤوس والتذييلات المقابلة لها في القسم السابق. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious)(*[HeaderFooterType](../headerfootertype/), bool*) | يربط أو يلغي ربط الرأس أو التذييل المحدد بالرأس أو التذييل المقابل في القسم السابق. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | يزيل العقدة من المجموعة ومن المستند. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | يزيل العقدة الموجودة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](../../aspose.words/headerfootercollection/toarray/#toarray)() | نسخ الكل`رأس وتذييل` من المجموعة إلى مجموعة جديدة من`رأس وتذييل` س. (2 methods) |

## ملاحظات

يمكن أن يكون هناك حد أقصى واحد[`HeaderFooter`](../headerfooter/)

من كل واحد[`HeaderFooterType`](../headerfootertype/) لكل x000d_[`Section`](../section/) .

[`HeaderFooter`](../headerfooter/) يمكن أن تظهر الكائنات بأي ترتيب في المجموعة.

## أمثلة

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

يوضح كيفية إنشاء رأس وتذييل.

```csharp
Document doc = new Document();

// أنشئ رأسًا وأضف إليه فقرة. النص في تلك الفقرة
// سوف تظهر في أعلى كل صفحة من هذا القسم، فوق النص الرئيسي.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// أنشئ تذييلًا وأضف إليه فقرة. النص في تلك الفقرة
// سوف تظهر في أسفل كل صفحة من هذا القسم، أسفل النص الرئيسي.
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
