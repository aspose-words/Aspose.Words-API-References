---
title: ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle
linktitle: NoSpaceBetweenParagraphsOfSameStyle
articleTitle: NoSpaceBetweenParagraphsOfSameStyle
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ParagraphFormat NoSpaceBetweenParagraphsOfSameStyle. حسّن تصميم مستندك بإزالة المسافات بين الفقرات المتشابهة.
type: docs
weight: 250
url: /ar/net/aspose.words/paragraphformat/nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle property

عندما`حقيقي` ،[`SpaceBefore`](../spacebefore/) و[`SpaceAfter`](../spaceafter/) سيتم تجاهل بين الفقرات ذات نفس النمط.

```csharp
public bool NoSpaceBetweenParagraphsOfSameStyle { get; set; }
```

## ملاحظات

لا يُطبَّق هذا الإعداد إلا على نمط فقرة. أما إذا طُبِّق مباشرةً على فقرة، فلن يكون له أي تأثير.

## أمثلة

يوضح كيفية عدم تطبيق المسافة بين الفقرات بنفس النمط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتطبيق قدر كبير من التباعد قبل وبعد الفقرات التي سيقوم هذا المنشئ بإنشائها.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// اضبط علامة "NoSpaceBetweenParagraphsOfSameStyle" على "true" لتطبيقها
// لا توجد مسافة بين الفقرات التي لها نفس النمط، مما سيؤدي إلى تجميع الفقرات المتشابهة.
// اترك علامة "NoSpaceBetweenParagraphsOfSameStyle" على "false"
// لتطبيق التباعد بالتساوي على كل فقرة.
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
