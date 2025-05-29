---
title: Document.AppendDocument
linktitle: AppendDocument
articleTitle: AppendDocument
second_title: Aspose.Words لـ .NET
description: أضف المستندات بسهولة مع طريقة إضافة المستندات لدينا. حسّن سير عملك من خلال دمج المحتوى بسلاسة في ملفاتك الحالية.
type: docs
weight: 570
url: /ar/net/aspose.words/document/appenddocument/
---
## AppendDocument(*[Document](../), [ImportFormatMode](../../importformatmode/)*) {#appenddocument}

يضيف المستند المحدد إلى نهاية هذا المستند.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcDoc | Document | الوثيقة المراد إضافتها. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيقات الأنماط المتعارضة. |

## أمثلة

يوضح كيفية إضافة مستند إلى نهاية مستند آخر.

```csharp
Document srcDoc = new Document();
srcDoc.FirstSection.Body.AppendParagraph("Source document text. ");

Document dstDoc = new Document();
dstDoc.FirstSection.Body.AppendParagraph("Destination document text. ");

// إضافة المستند المصدر إلى المستند الوجهة مع الحفاظ على تنسيقه،
// ثم قم بحفظ المستند المصدر في نظام الملفات المحلي.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
dstDoc.Save(ArtifactsDir + "Document.AppendDocument.docx");
```

يوضح كيفية إضافة جميع المستندات الموجودة في مجلد إلى نهاية مستند القالب.

```csharp
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Template Document");
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Some content here");
// إضافة جميع المستندات غير المشفرة ذات الامتداد .doc
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## AppendDocument(*[Document](../), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#appenddocument_1}

يضيف المستند المحدد إلى نهاية هذا المستند.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcDoc | Document | الوثيقة المراد إضافتها. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيقات الأنماط المتعارضة. |
| importFormatOptions | ImportFormatOptions | يسمح بتحديد الخيارات التي تؤثر على تنسيق المستند الناتج. |

## أمثلة

يوضح كيفية إدارة تعارضات نمط القائمة أثناء إضافة نسخة من المستند إلى نفسها.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List item.docx");

// إذا كان هناك تعارض بين أنماط القائمة، قم بتطبيق تنسيق القائمة الخاص بالمستند المصدر.
// قم بتعيين خاصية "KeepSourceNumbering" إلى "false" لعدم استيراد أي أرقام قائمة إلى المستند الوجهة.
// اضبط خاصية "KeepSourceNumbering" على "true" لاستيراد جميع البيانات المتضاربة
// ترقيم نمط القائمة بنفس المظهر الذي كان عليه في المستند المصدر.
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

// إذا كان هناك تعارض بين أنماط القائمة، قم بتطبيق تنسيق القائمة الخاص بالمستند المصدر.
// قم بتعيين خاصية "KeepSourceNumbering" إلى "false" لعدم استيراد أي أرقام قائمة إلى المستند الوجهة.
// اضبط خاصية "KeepSourceNumbering" على "true" لاستيراد جميع البيانات المتضاربة
// ترقيم نمط القائمة بنفس المظهر الذي كان عليه في المستند المصدر.
ImportFormatOptions importOptions = new ImportFormatOptions();
importOptions.KeepSourceNumbering = keepSourceNumbering;

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertDocument(attachDoc, ImportFormatMode.KeepSourceFormatting, importOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```

يوضح كيفية إدارة تعارضات نمط القائمة أثناء إضافة مستند.

```csharp
// قم بتحميل مستند يحتوي على نص بأسلوب مخصص ثم استنساخه.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// لدينا الآن مستندين، كل منهما بنفس النمط المسمى "CustomStyle".
// قم بتغيير لون النص لأحد الأنماط لتمييزه عن الآخر.
dstDoc.Styles["CustomStyle"].Font.Color = Color.DarkRed;

// إذا كان هناك تعارض بين أنماط القائمة، قم بتطبيق تنسيق القائمة الخاص بالمستند المصدر.
// قم بتعيين خاصية "KeepSourceNumbering" إلى "false" لعدم استيراد أي أرقام قائمة إلى المستند الوجهة.
// اضبط خاصية "KeepSourceNumbering" على "true" لاستيراد جميع البيانات المتضاربة
// ترقيم نمط القائمة بنفس المظهر الذي كان عليه في المستند المصدر.
ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;

// يؤدي ضم مستندين لهما أنماط مختلفة تشتركان في نفس الاسم إلى حدوث تعارض في الأنماط.
// يمكننا تحديد وضع تنسيق الاستيراد أثناء إلحاق المستندات لحل هذا التعارض.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepDifferentStyles, options);
dstDoc.UpdateListLabels();

dstDoc.Save(ArtifactsDir + "DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```

### أنظر أيضا

* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
