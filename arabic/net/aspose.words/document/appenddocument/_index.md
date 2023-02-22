---
title: Document.AppendDocument
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. إلحاق المستند المحدد بنهاية هذا المستند.
type: docs
weight: 510
url: /ar/net/aspose.words/document/appenddocument/
---
## AppendDocument(Document, ImportFormatMode) {#appenddocument}

إلحاق المستند المحدد بنهاية هذا المستند.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcDoc | Document | المستند المطلوب إلحاقه. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيق النمط الذي يتعارض. |

### أمثلة

يوضح كيفية إلحاق مستند بنهاية مستند آخر.

```csharp
Document srcDoc = new Document();
srcDoc.FirstSection.Body.AppendParagraph("Source document text. ");

Document dstDoc = new Document();
dstDoc.FirstSection.Body.AppendParagraph("Destination document text. ");

// إلحاق المستند المصدر بالمستند الوجهة مع الحفاظ على تنسيقه ،
// ثم احفظ المستند المصدر في نظام الملفات المحلي.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
dstDoc.Save(ArtifactsDir + "Document.AppendDocument.docx");
```

يوضح كيفية إلحاق كافة المستندات الموجودة في مجلد بنهاية مستند القالب.

```csharp
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Template Document");
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Some content here");

// قم بإلحاق كافة المستندات غير المشفرة بامتداد .doc
// من دليل نظام الملفات المحلي إلى المستند الأساسي.
List<string> docFiles = Directory.GetFiles(MyDir, "*.doc").Where(item => item.EndsWith(".doc")).ToList();
foreach (string fileName in docFiles)
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(fileName);
    if (info.IsEncrypted)
        continue;

    Document srcDoc = new Document(fileName);
    dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles);
}

dstDoc.Save(ArtifactsDir + "Document.AppendAllDocumentsInFolder.doc");
```

### أنظر أيضا

* enum [ImportFormatMode](../../importformatmode/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)

---

## AppendDocument(Document, ImportFormatMode, ImportFormatOptions) {#appenddocument_1}

إلحاق المستند المحدد بنهاية هذا المستند.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcDoc | Document | المستند المطلوب إلحاقه. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيق النمط الذي يتعارض. |
| importFormatOptions | ImportFormatOptions | يسمح بتحديد الخيارات التي تؤثر على تنسيق الوثيقة الناتجة. |

### أمثلة

يوضح كيفية إدارة تعارضات نمط القائمة أثناء إلحاق نسخة من المستند بنفسها.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List item.docx");

// إذا كان هناك تضارب في أنماط القائمة ، فقم بتطبيق تنسيق القائمة الخاص بالمستند المصدر.
// اضبط خاصية "KeepSourceNumbering" على "false" لعدم استيراد أي أرقام قائمة إلى المستند الوجهة.
// اضبط خاصية "KeepSourceNumbering" على "true" لاستيراد كل التعارضات
// قائمة ترقيم نمط مع نفس المظهر الذي كان عليه في المستند المصدر.
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.SectionBreakNewPage);

ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;
builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.UpdateListLabels();
```

يوضح كيفية إدارة تعارضات نمط القائمة أثناء إدراج مستند.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.InsertBreak(BreakType.ParagraphBreak);

dstDoc.Lists.Add(ListTemplate.NumberDefault);
Aspose.Words.Lists.List list = dstDoc.Lists[0];

builder.ListFormat.List = list;

for (int i = 1; i <= 15; i++)
    builder.Write($"List Item {i}\n");

Document attachDoc = (Document)dstDoc.Clone(true);

// إذا كان هناك تضارب في أنماط القائمة ، فقم بتطبيق تنسيق القائمة الخاص بالمستند المصدر.
// اضبط خاصية "KeepSourceNumbering" على "false" لعدم استيراد أي أرقام قائمة إلى المستند الوجهة.
// اضبط خاصية "KeepSourceNumbering" على "true" لاستيراد كل التعارضات
// قائمة ترقيم نمط مع نفس المظهر الذي كان عليه في المستند المصدر.
ImportFormatOptions importOptions = new ImportFormatOptions();
importOptions.KeepSourceNumbering = keepSourceNumbering;

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertDocument(attachDoc, ImportFormatMode.KeepSourceFormatting, importOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```

يوضح كيفية إدارة تعارضات نمط القائمة أثناء إلحاق مستند.

```csharp
// قم بتحميل مستند بنص بنمط مخصص وقم بنسخه.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// لدينا الآن وثيقتان ، لكل منهما نمط مماثل يسمى "CustomStyle".
// تغيير لون النص لأحد الأنماط لتمييزه عن الآخر.
dstDoc.Styles["CustomStyle"].Font.Color = Color.DarkRed;

// إذا كان هناك تضارب في أنماط القائمة ، فقم بتطبيق تنسيق القائمة الخاص بالمستند المصدر.
// اضبط خاصية "KeepSourceNumbering" على "false" لعدم استيراد أي أرقام قائمة إلى المستند الوجهة.
// اضبط خاصية "KeepSourceNumbering" على "true" لاستيراد كل التعارضات
// قائمة ترقيم نمط مع نفس المظهر الذي كان عليه في المستند المصدر.
ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;

// يؤدي ضم مستندين لهما أنماط مختلفة تشترك في نفس الاسم إلى تعارض في النمط.
// يمكننا تحديد وضع تنسيق الاستيراد أثناء إلحاق المستندات لحل هذا التعارض.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepDifferentStyles, options);
dstDoc.UpdateListLabels();

dstDoc.Save(ArtifactsDir + "DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```

### أنظر أيضا

* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


