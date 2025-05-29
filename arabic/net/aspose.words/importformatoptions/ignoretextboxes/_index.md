---
title: ImportFormatOptions.IgnoreTextBoxes
linktitle: IgnoreTextBoxes
articleTitle: IgnoreTextBoxes
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية ImportFormatOptions IgnoreTextBoxes تنسيق مستندك من خلال التحكم في محتوى مربع النص. حسّنه بسهولة اليوم!
type: docs
weight: 50
url: /ar/net/aspose.words/importformatoptions/ignoretextboxes/
---
## ImportFormatOptions.IgnoreTextBoxes property

يحصل على قيمة منطقية تحدد تنسيق المصدر لمحتوى مربعات النص أو يعينها. يتم تجاهل إذاKeepSourceFormatting يتم استخدام الوضع. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool IgnoreTextBoxes { get; set; }
```

## أمثلة

يوضح كيفية إدارة تنسيق مربع النص أثناء إضافة مستند.

```csharp
// قم بإنشاء مستند سيحتوي على عقد من مستند آخر مدرجة فيه.
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

builder.Writeln("Hello world!");

// قم بإنشاء مستند آخر يحتوي على مربع نص، والذي سنقوم باستيراده إلى المستند الأول.
Document srcDoc = new Document();
builder = new DocumentBuilder(srcDoc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 300, 100);
builder.MoveTo(textBox.FirstParagraph);
builder.ParagraphFormat.Style.Font.Name = "Courier New";
builder.ParagraphFormat.Style.Font.Size = 24;
builder.Write("Textbox contents");

// تعيين علامة لتحديد ما إذا كان سيتم مسح تنسيق مربع النص أو الحفاظ عليه
//أثناء استيرادها إلى مستندات أخرى.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreTextBoxes = ignoreTextBoxes;

// استيراد مربع النص من المستند المصدر إلى المستند الوجهة،
// ثم تأكد ما إذا كنا قد حافظنا على تنسيق محتويات النص.
NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);
Shape importedTextBox = (Shape)importer.ImportNode(textBox, true);
dstDoc.FirstSection.Body.Paragraphs[1].AppendChild(importedTextBox);

if (ignoreTextBoxes)
{
    Assert.AreEqual(12.0d, importedTextBox.FirstParagraph.Runs[0].Font.Size);
    Assert.AreEqual("Times New Roman", importedTextBox.FirstParagraph.Runs[0].Font.Name);
}
else
{
    Assert.AreEqual(24.0d, importedTextBox.FirstParagraph.Runs[0].Font.Size);
    Assert.AreEqual("Courier New", importedTextBox.FirstParagraph.Runs[0].Font.Name);
}

dstDoc.Save(ArtifactsDir + "DocumentBuilder.IgnoreTextBoxes.docx");
```

### أنظر أيضا

* class [ImportFormatOptions](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
