---
title: PageSetup.EndnoteOptions
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageSetup EndnoteOptions لتخصيص ترقيم الملاحظات الختامية وتحديد موضعها بسهولة لتحسين تنسيق المستند ووضوحه.
type: docs
weight: 120
url: /ar/net/aspose.words/pagesetup/endnoteoptions/
---
## PageSetup.EndnoteOptions property

يوفر خيارات للتحكم في ترقيم وموضع الحواشي الختامية في هذا القسم.

```csharp
public EndnoteOptions EndnoteOptions { get; }
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

* class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
