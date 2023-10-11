---
title: Document.AppendDocument
second_title: Aspose.Words لمراجع .NET API
description: Document طريقة. إلحاق المستند المحدد بنهاية هذا المستند.
type: docs
weight: 550
url: /ar/net/aspose.words/document/appenddocument/
---
## AppendDocument(Document, ImportFormatMode) {#appenddocument}

إلحاق المستند المحدد بنهاية هذا المستند.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcDoc | Document | الوثيقة المراد إلحاقها. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيقات النمط التي تتعارض. |

### أمثلة

يوضح كيفية إلحاق مستند بنهاية مستند آخر.

```csharp
Document srcDoc = new Document();
srcDoc.FirstSection.Body.AppendParagraph("Source document text. ");

Document dstDoc = new Document();
dstDoc.FirstSection.Body.AppendParagraph("Destination document text. ");

// إلحاق المستند المصدر بالمستند الوجهة مع الحفاظ على تنسيقه،
// ثم احفظ المستند المصدر في نظام الملفات المحلي.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
dstDoc.Save(ArtifactsDir + "Document.AppendDocument.docx");
```

يوضح كيفية إلحاق جميع المستندات الموجودة في مجلد بنهاية مستند القالب.

```csharp
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Template Document");
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Some content here");
// إلحاق جميع المستندات غير المشفرة بامتداد .doc
// من دليل نظام الملفات المحلي الخاص بنا إلى المستند الأساسي.
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
| srcDoc | Document | الوثيقة المراد إلحاقها. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيقات النمط التي تتعارض. |
| importFormatOptions | ImportFormatOptions | يسمح بتحديد الخيارات التي تؤثر على تنسيق مستند النتيجة. |

### أمثلة

يوضح كيفية إدارة تضارب أنماط القائمة أثناء إلحاق نسخة من المستند بنفسها.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List item.docx");

// إذا كان هناك تعارض بين أنماط القائمة، فقم بتطبيق تنسيق القائمة الخاص بالمستند المصدر.
// قم بتعيين خاصية "KeepSourceNumbering" على "خطأ" لعدم استيراد أي أرقام قائمة إلى المستند الوجهة.
// اضبط خاصية "KeepSourceNumbering" على "صحيح" لاستيراد كل التضارب
// ترقيم نمط القائمة بنفس المظهر الموجود في المستند المصدر.
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.SectionBreakNewPage);

ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;
builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.UpdateListLabels();
```

يوضح كيفية إدارة تضارب أنماط القائمة أثناء إدراج مستند.

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

// إذا كان هناك تعارض بين أنماط القائمة، فقم بتطبيق تنسيق القائمة الخاص بالمستند المصدر.
// قم بتعيين خاصية "KeepSourceNumbering" على "خطأ" لعدم استيراد أي أرقام قائمة إلى المستند الوجهة.
// اضبط خاصية "KeepSourceNumbering" على "صحيح" لاستيراد كل التضارب
// ترقيم نمط القائمة بنفس المظهر الموجود في المستند المصدر.
ImportFormatOptions importOptions = new ImportFormatOptions();
importOptions.KeepSourceNumbering = keepSourceNumbering;

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertDocument(attachDoc, ImportFormatMode.KeepSourceFormatting, importOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```

يوضح كيفية إدارة تضارب أنماط القائمة أثناء إلحاق مستند.

```csharp
// قم بتحميل مستند يحتوي على نص بنمط مخصص ثم قم باستنساخه.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// لدينا الآن وثيقتان، لكل منهما نمط متطابق يسمى "CustomStyle".
// قم بتغيير لون النص لأحد الأنماط لتمييزه عن الآخر.
dstDoc.Styles["CustomStyle"].Font.Color = Color.DarkRed;

// إذا كان هناك تعارض بين أنماط القائمة، فقم بتطبيق تنسيق القائمة الخاص بالمستند المصدر.
// قم بتعيين خاصية "KeepSourceNumbering" على "خطأ" لعدم استيراد أي أرقام قائمة إلى المستند الوجهة.
// اضبط خاصية "KeepSourceNumbering" على "صحيح" لاستيراد كل التضارب
// ترقيم نمط القائمة بنفس المظهر الموجود في المستند المصدر.
ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;

// يؤدي الانضمام إلى مستندين لهما أنماط مختلفة تشترك في نفس الاسم إلى حدوث تعارض في النمط.
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


