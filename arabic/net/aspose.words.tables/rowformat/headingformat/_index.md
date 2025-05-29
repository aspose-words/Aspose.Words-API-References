---
title: RowFormat.HeadingFormat
linktitle: HeadingFormat
articleTitle: HeadingFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية RowFormat HeadingFormat، وتأكد من تكرار عناوين الجدول في كل صفحة لتحقيق الوضوح وتحسين إمكانية القراءة في المستندات متعددة الصفحات.
type: docs
weight: 30
url: /ar/net/aspose.words.tables/rowformat/headingformat/
---
## RowFormat.HeadingFormat property

صحيح إذا تم تكرار الصف كعنوان جدول في كل صفحة عندما يمتد الجدول إلى أكثر من صفحة واحدة.

```csharp
public bool HeadingFormat { get; set; }
```

## أمثلة

يوضح كيفية إنشاء جدول يحتوي على صفوف تتكرر في كل صفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// أي صفوف تم إدراجها أثناء تعيين علم "HeadingFormat" على "true"
//سيظهر في أعلى الجدول في كل صفحة يمتد فيها.
builder.RowFormat.HeadingFormat = true;
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.CellFormat.Width = 100;
builder.InsertCell();
builder.Write("Heading row 1");
builder.EndRow();
builder.InsertCell();
builder.Write("Heading row 2");
builder.EndRow();

builder.CellFormat.Width = 50;
builder.ParagraphFormat.ClearFormatting();
builder.RowFormat.HeadingFormat = false;

//أضف عددًا كافيًا من الصفوف لكي يمتد الجدول على صفحتين.
for (int i = 0; i < 50; i++)
{
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 1.");
    builder.InsertCell();
    builder.Write($"Row {table.Rows.Count}, column 2.");
    builder.EndRow();
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableSetHeadingRow.docx");
```

### أنظر أيضا

* class [RowFormat](../)
* مساحة الاسم [Aspose.Words.Tables](../../../aspose.words.tables/)
* المجسم [Aspose.Words](../../../)
