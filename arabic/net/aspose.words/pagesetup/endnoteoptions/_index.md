---
title: PageSetup.EndnoteOptions
second_title: Aspose.Words لمراجع .NET API
description: PageSetup ملكية. يوفر خيارات تتحكم في ترقيم وموضع التعليقات الختامية في هذا القسم.
type: docs
weight: 120
url: /ar/net/aspose.words/pagesetup/endnoteoptions/
---
## PageSetup.EndnoteOptions property

يوفر خيارات تتحكم في ترقيم وموضع التعليقات الختامية في هذا القسم.

```csharp
public EndnoteOptions EndnoteOptions { get; }
```

### أمثلة

يوضح كيفية تكوين الخيارات التي تؤثر على الحواشي السفلية / التعليقات الختامية في القسم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote reference text.");

// تكوين جميع الحواشي السفلية في القسم الأول لإعادة تشغيل الترقيم من 1
// في كل صفحة جديدة وتعرض نفسها مباشرة أسفل النص في كل صفحة.
FootnoteOptions footnoteOptions = doc.Sections[0].PageSetup.FootnoteOptions;
footnoteOptions.Position = FootnotePosition.BeneathText;
footnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
footnoteOptions.StartNumber = 1;

builder.Write(" Hello again.");
builder.InsertFootnote(FootnoteType.Footnote, "Endnote reference text.");

// تكوين جميع التعليقات الختامية في القسم الأول للحفاظ على العد المستمر في جميع أنحاء القسم ،
// بدءًا من 1. أيضًا ، قم بتعيينها جميعًا لتظهر مجمعة في نهاية المستند.
EndnoteOptions endnoteOptions = doc.Sections[0].PageSetup.EndnoteOptions;
endnoteOptions.Position = EndnotePosition.EndOfDocument;
endnoteOptions.RestartRule = FootnoteNumberingRule.Continuous;
endnoteOptions.StartNumber = 1;

doc.Save(ArtifactsDir + "PageSetup.FootnoteOptions.docx");
```

### أنظر أيضا

* class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../pagesetup/)
* المجسم [Aspose.Words](../../../)


