---
title: Processor Class
linktitle: Processor
articleTitle: Processor
second_title: Aspose.Words لـ .NET
description: قم بتعزيز معالجة المستندات باستخدام فئة Aspose.Words.LowCode.Processor، المصممة للتعامل بسلاسة وكفاءة مع مهام المستندات المختلفة.
type: docs
weight: 4320
url: /ar/net/aspose.words.lowcode/processor/
---
## Processor class

فئة المعالج لأداء إجراءات معالجة المستندات المختلفة.

```csharp
public class Processor
```

## طُرق

| اسم | وصف |
| --- | --- |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | تنفيذ إجراء المعالج. |
| [From](../../aspose.words.lowcode/processor/from/#from)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | يحدد مستند الإدخال للمعالجة. |
| [From](../../aspose.words.lowcode/processor/from/#from_1)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | يحدد مستند الإدخال للمعالجة. |
| [To](../../aspose.words.lowcode/processor/to/#to)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | يحدد قائمة تدفقات المستندات الناتجة. |
| [To](../../aspose.words.lowcode/processor/to/#to_1)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحدد قائمة تدفقات المستندات الناتجة. |
| [To](../../aspose.words.lowcode/processor/to/#to_2)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | يحدد تدفق الإخراج للمعالج. |
| [To](../../aspose.words.lowcode/processor/to/#to_3)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحدد تدفق الإخراج للمعالج. |
| [To](../../aspose.words.lowcode/processor/to/#to_4)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | يحدد ملف الإخراج للمعالج. |
| [To](../../aspose.words.lowcode/processor/to/#to_5)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | يحدد ملف الإخراج للمعالج. |

## أمثلة

يوضح كيفية تحويل المستندات بسطر واحد من التعليمات البرمجية باستخدام السياق.

```csharp
string doc = MyDir + "Big document.docx";

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.1.pdf")
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.2.pdf", SaveFormat.Rtf)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Create(new ConverterContext())
    .From(doc, loadOptions)
    .To(ArtifactsDir + "LowCode.ConvertContext.3.docx", saveOptions)
    .Execute();

Converter.Create(new ConverterContext())
    .From(doc)
    .To(ArtifactsDir + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.Png))
    .Execute();
```

يوضح كيفية إجراء عملية دمج البريد من جدول بيانات باستخدام المستندات من التدفق باستخدام السياق.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد من جدول بيانات باستخدام المستندات من التدفق:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(dataTable);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamDataTable.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

يوضح كيفية تحويل المستندات من مجرى باستخدام سطر واحد من التعليمات البرمجية باستخدام السياق.

```csharp
string doc = MyDir + "Document.docx";
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn)
            .To(streamOut, SaveFormat.Rtf)
            .Execute();

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertContextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Create(new ConverterContext())
            .From(streamIn, loadOptions)
            .To(streamOut, saveOptions)
            .Execute();

    List<Stream> pages = new List<Stream>();
    Converter.Create(new ConverterContext())
        .From(doc)
        .To(pages, new ImageSaveOptions(SaveFormat.Png))
        .Execute();
}
```

يوضح كيفية دمج المستندات في مستند إخراج واحد باستخدام السياق.

```csharp
//هناك عدة طرق لدمج المستندات:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.1.docx")
    .Execute();

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1, firstLoadOptions)
    .From(inputDoc2, secondLoadOptions)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.2.docx", SaveFormat.Docx)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.3.docx", saveOptions)
    .Execute();
```

يوضح كيفية دمج المستندات من التدفق إلى مستند إخراج واحد باستخدام السياق.

```csharp
//هناك عدة طرق لدمج المستندات:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn)
            .From(secondStreamIn)
            .To(streamOut, saveOptions)
            .Execute();

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn, firstLoadOptions)
            .From(secondStreamIn, secondLoadOptions)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
    }
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../)
