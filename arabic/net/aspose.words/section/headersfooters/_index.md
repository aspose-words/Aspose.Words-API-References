---
title: Section.HeadersFooters
second_title: Aspose.Words لمراجع .NET API
description: Section ملكية. يوفر الوصول إلى رؤوس وتذييلات العقد الخاصة بالقسم.
type: docs
weight: 30
url: /ar/net/aspose.words/section/headersfooters/
---
## Section.HeadersFooters property

يوفر الوصول إلى رؤوس وتذييلات العقد الخاصة بالقسم.

```csharp
public HeaderFooterCollection HeadersFooters { get; }
```

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

* class [HeaderFooterCollection](../../headerfootercollection/)
* class [Section](../)
* مساحة الاسم [Aspose.Words](../../section/)
* المجسم [Aspose.Words](../../../)


