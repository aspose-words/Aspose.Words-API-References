---
title: TableContentAlignment Enum
linktitle: TableContentAlignment
articleTitle: TableContentAlignment
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.Saving.TableContentAlignment لمحاذاة محتوى الجدول بدقة عند تصدير Markdown. حسّن تنسيق مستنداتك بسهولة!
type: docs
weight: 6420
url: /ar/net/aspose.words.saving/tablecontentalignment/
---
## TableContentAlignment enumeration

يسمح بتحديد محاذاة محتوى الجدول الذي سيتم استخدامه عند التصدير إلى تنسيق Markdown.

```csharp
public enum TableContentAlignment
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Auto | `0` | سيتم أخذ المحاذاة من الفقرة الأولى في عمود الجدول المقابل. |
| Left | `1` | سيتم محاذاة محتوى الجداول إلى اليسار. |
| Center | `2` | سيتم محاذاة محتوى الجداول إلى المركز. |
| Right | `3` | سيتم محاذاة محتوى الجداول إلى اليمين. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
