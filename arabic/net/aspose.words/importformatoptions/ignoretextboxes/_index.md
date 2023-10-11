---
title: ImportFormatOptions.IgnoreTextBoxes
second_title: Aspose.Words لمراجع .NET API
description: ImportFormatOptions ملكية. الحصول على أو تعيين قيمة منطقية تحدد تنسيق المصدر لمحتوى مربعات النص الذي تم تجاهله إذاKeepSourceFormatting يتم استخدام الوضع. القيمة الافتراضية هيحقيقي .
type: docs
weight: 50
url: /ar/net/aspose.words/importformatoptions/ignoretextboxes/
---
## ImportFormatOptions.IgnoreTextBoxes property

الحصول على أو تعيين قيمة منطقية تحدد تنسيق المصدر لمحتوى مربعات النص الذي تم تجاهله إذاKeepSourceFormatting يتم استخدام الوضع. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool IgnoreTextBoxes { get; set; }
```

### أمثلة

يوضح كيفية إدارة تنسيق مربع النص أثناء إلحاق مستند.

```csharp
// قم بإنشاء مستند سيتم إدراج عقد من مستند آخر فيه.
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

builder.Writeln("Hello world!");

// أنشئ مستندًا آخر يحتوي على مربع نص، وسنقوم باستيراده إلى المستند الأول.
Document srcDoc = new Document();
builder = new DocumentBuilder(srcDoc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 300, 100);
builder.MoveTo(textBox.FirstParagraph);
builder.ParagraphFormat.Style.Font.Name = "Courier New";
builder.ParagraphFormat.Style.Font.Size = 24;
builder.Write("Textbox contents");

// قم بتعيين علامة لتحديد ما إذا كنت تريد مسح تنسيق مربع النص أو الحفاظ عليه
// أثناء استيرادها إلى مستندات أخرى.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreTextBoxes = ignoreTextBoxes;

// قم باستيراد مربع النص من المستند المصدر إلى المستند الوجهة،
// ثم تحقق مما إذا كنا قد حافظنا على تصميم محتويات النص الخاص به.
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
* مساحة الاسم [Aspose.Words](../../importformatoptions/)
* المجسم [Aspose.Words](../../../)


