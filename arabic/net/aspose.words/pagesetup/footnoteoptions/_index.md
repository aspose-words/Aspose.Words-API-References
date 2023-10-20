---
title: PageSetup.FootnoteOptions
linktitle: FootnoteOptions
articleTitle: FootnoteOptions
second_title: Aspose.Words لـ .NET
description: PageSetup FootnoteOptions ملكية. يوفر خيارات تتحكم في ترقيم الحواشي السفلية وموضعها في هذا القسم في C#.
type: docs
weight: 150
url: /ar/net/aspose.words/pagesetup/footnoteoptions/
---
## PageSetup.FootnoteOptions property

يوفر خيارات تتحكم في ترقيم الحواشي السفلية وموضعها في هذا القسم.

```csharp
public FootnoteOptions FootnoteOptions { get; }
```

## أمثلة

يوضح كيفية تكوين الخيارات التي تؤثر على الحواشي السفلية/التعليقات الختامية في القسم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote reference text.");

// قم بتكوين كافة الحواشي السفلية في القسم الأول لإعادة تشغيل الترقيم من 1
// في كل صفحة جديدة ويعرضون أنفسهم مباشرة أسفل النص في كل صفحة.
FootnoteOptions footnoteOptions = doc.Sections[0].PageSetup.FootnoteOptions;
footnoteOptions.Position = FootnotePosition.BeneathText;
footnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
footnoteOptions.StartNumber = 1;

builder.Write(" Hello again.");
builder.InsertFootnote(FootnoteType.Footnote, "Endnote reference text.");

// قم بتكوين جميع التعليقات الختامية في القسم الأول للحفاظ على العدد المستمر في جميع أنحاء القسم،
// بدءًا من 1. قم أيضًا بتعيينها جميعًا لتظهر مجمعة في نهاية المستند.
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
