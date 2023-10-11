---
title: Story.AppendParagraph
second_title: Aspose.Words لمراجع .NET API
description: Story طريقة. طريقة اختصار لإنشاء ملفParagraph كائن بنص اختياري وإلحاقه بنهاية هذا الكائن.
type: docs
weight: 60
url: /ar/net/aspose.words/story/appendparagraph/
---
## Story.AppendParagraph method

طريقة اختصار لإنشاء ملف[`Paragraph`](../../paragraph/) كائن بنص اختياري وإلحاقه بنهاية هذا الكائن.

```csharp
public Paragraph AppendParagraph(string text)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| text | String | النص للفقرة. يمكن ان يكون`باطل` أو سلسلة فارغة. |

### قيمة الإرجاع

الفقرة التي تم إنشاؤها وإلحاقها حديثًا.

### أمثلة

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

* class [Paragraph](../../paragraph/)
* class [Story](../)
* مساحة الاسم [Aspose.Words](../../story/)
* المجسم [Aspose.Words](../../../)


