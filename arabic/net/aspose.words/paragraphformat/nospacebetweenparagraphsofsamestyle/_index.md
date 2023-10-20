---
title: ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle
linktitle: NoSpaceBetweenParagraphsOfSameStyle
articleTitle: NoSpaceBetweenParagraphsOfSameStyle
second_title: Aspose.Words لـ .NET
description: ParagraphFormat NoSpaceBetweenParagraphsOfSameStyle ملكية. متىحقيقي SpaceBefore وSpaceAfter سيتم تجاهل بين الفقرات ذات نفس النمط في C#.
type: docs
weight: 240
url: /ar/net/aspose.words/paragraphformat/nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle property

متى`حقيقي` ,[`SpaceBefore`](../spacebefore/) و[`SpaceAfter`](../spaceafter/) سيتم تجاهل بين الفقرات ذات نفس النمط.

```csharp
public bool NoSpaceBetweenParagraphsOfSameStyle { get; set; }
```

## ملاحظات

لا يسري هذا الإعداد إلا عند تطبيقه على نمط الفقرة. إذا تم تطبيقه على فقرة مباشرة، فلن يكون له أي تأثير.

## أمثلة

يوضح كيفية تطبيق عدم وجود مسافات بين الفقرات بنفس النمط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتطبيق قدر كبير من التباعد قبل وبعد الفقرات التي سينشئها هذا المنشئ.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// قم بتعيين علامة "NoSpaceBetweenParagraphsOfSameStyle" على "صحيح" للتطبيق
// لا توجد مسافات بين الفقرات ذات النمط نفسه، مما يؤدي إلى تجميع الفقرات المتشابهة.
// اترك علامة "NoSpaceBetweenParagraphsOfSameStyle" على أنها "خطأ"
// لتطبيق المسافات بالتساوي على كل فقرة.
builder.ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle = noSpaceBetweenParagraphsOfSameStyle;

builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
