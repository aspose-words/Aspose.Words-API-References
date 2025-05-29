---
title: MarkdownSaveOptions.TableContentAlignment
linktitle: TableContentAlignment
articleTitle: TableContentAlignment
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MarkdownSaveOptions TableContentAlignment لتخصيص محاذاة محتوى الجدول لتصدير Markdown بسلاسة. الإعداد الافتراضي هو "تلقائي".
type: docs
weight: 140
url: /ar/net/aspose.words.saving/markdownsaveoptions/tablecontentalignment/
---
## MarkdownSaveOptions.TableContentAlignment property

يحصل على قيمة تحدد كيفية محاذاة المحتويات في tables عند التصدير إلىMarkdown format. القيمة الافتراضية هيAuto .

```csharp
public TableContentAlignment TableContentAlignment { get; set; }
```

## أمثلة

يوضح كيفية محاذاة المحتويات في الجداول.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;
builder.Write("Cell1");
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write("Cell2");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions { TableContentAlignment = tableContentAlignment };

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md", saveOptions);

Document doc = new Document(ArtifactsDir + "MarkdownSaveOptions.MarkdownDocumentTableContentAlignment.md");
Table table = doc.FirstSection.Body.Tables[0];

switch (tableContentAlignment)
{
    case TableContentAlignment.Auto:
        Assert.AreEqual(ParagraphAlignment.Right,
            table.FirstRow.Cells[0].FirstParagraph.ParagraphFormat.Alignment);
        Assert.AreEqual(ParagraphAlignment.Center,
            table.FirstRow.Cells[1].FirstParagraph.ParagraphFormat.Alignment);
        break;
    case TableContentAlignment.Left:
        Assert.AreEqual(ParagraphAlignment.Left,
            table.FirstRow.Cells[0].FirstParagraph.ParagraphFormat.Alignment);
        Assert.AreEqual(ParagraphAlignment.Left,
            table.FirstRow.Cells[1].FirstParagraph.ParagraphFormat.Alignment);
        break;
    case TableContentAlignment.Center:
        Assert.AreEqual(ParagraphAlignment.Center,
            table.FirstRow.Cells[0].FirstParagraph.ParagraphFormat.Alignment);
        Assert.AreEqual(ParagraphAlignment.Center,
            table.FirstRow.Cells[1].FirstParagraph.ParagraphFormat.Alignment);
        break;
    case TableContentAlignment.Right:
        Assert.AreEqual(ParagraphAlignment.Right,
            table.FirstRow.Cells[0].FirstParagraph.ParagraphFormat.Alignment);
        Assert.AreEqual(ParagraphAlignment.Right,
            table.FirstRow.Cells[1].FirstParagraph.ParagraphFormat.Alignment);
        break;
}
```

### أنظر أيضا

* enum [TableContentAlignment](../../tablecontentalignment/)
* class [MarkdownSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
