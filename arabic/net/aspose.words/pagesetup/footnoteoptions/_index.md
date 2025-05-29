---
title: PageSetup.FootnoteOptions
linktitle: FootnoteOptions
articleTitle: FootnoteOptions
second_title: Aspose.Words لـ .NET
description: اكتشف PageSetup FootnoteOptions لتخصيص ترقيم الحاشية السفلية وتحديد موقعها بسهولة لتحسين وضوح المستند واحترافيته.
type: docs
weight: 150
url: /ar/net/aspose.words/pagesetup/footnoteoptions/
---
## PageSetup.FootnoteOptions property

يوفر خيارات للتحكم في ترقيم الحواشي السفلية وتحديد موقعها في هذا القسم.

```csharp
public FootnoteOptions FootnoteOptions { get; }
```

## أمثلة

يوضح كيفية تكوين الخيارات التي تؤثر على الحواشي السفلية/الختامية في قسم ما.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote reference text.");

// قم بتكوين جميع الحواشي السفلية في القسم الأول لإعادة تشغيل الترقيم من 1
// في كل صفحة جديدة ويتم عرضها مباشرة أسفل النص في كل صفحة.
FootnoteOptions footnoteOptions = doc.Sections[0].PageSetup.FootnoteOptions;
footnoteOptions.Position = FootnotePosition.BeneathText;
footnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
footnoteOptions.StartNumber = 1;

builder.Write(" Hello again.");
builder.InsertFootnote(FootnoteType.Footnote, "Endnote reference text.");

// قم بتكوين جميع الحواشي الختامية في القسم الأول للحفاظ على عدد مستمر في جميع أنحاء القسم،
// بدءًا من 1. قم أيضًا بتعيينهم جميعًا ليظهروا مجمعين في نهاية المستند.
EndnoteOptions endnoteOptions = doc.Sections[0].PageSetup.EndnoteOptions;
endnoteOptions.Position = EndnotePosition.EndOfDocument;
endnoteOptions.RestartRule = FootnoteNumberingRule.Continuous;
endnoteOptions.StartNumber = 1;

doc.Save(ArtifactsDir + "PageSetup.FootnoteOptions.docx");
```

### أنظر أيضا

* class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
