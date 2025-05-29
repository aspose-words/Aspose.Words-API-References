---
title: Processor Class
linktitle: Processor
articleTitle: Processor
second_title: .NET için Aspose.Words
description: Çeşitli belge görevlerinin sorunsuz ve verimli bir şekilde işlenmesi için tasarlanan Aspose.Words.LowCode.Processor sınıfıyla belge işlemeyi geliştirin.
type: docs
weight: 4320
url: /tr/net/aspose.words.lowcode/processor/
---
## Processor class

Farklı belge işleme eylemlerini gerçekleştirmek için işlemci sınıfı.

```csharp
public class Processor
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | İşlemci eylemini yürüt. |
| [From](../../aspose.words.lowcode/processor/from/#from)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | İşleme için giriş belgesini belirtir. |
| [From](../../aspose.words.lowcode/processor/from/#from_1)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | İşleme için giriş belgesini belirtir. |
| [To](../../aspose.words.lowcode/processor/to/#to)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Çıktı Belge akışları listesini belirtir. |
| [To](../../aspose.words.lowcode/processor/to/#to_1)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Çıktı Belge akışları listesini belirtir. |
| [To](../../aspose.words.lowcode/processor/to/#to_2)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | İşlemci için çıkış akışını belirtir. |
| [To](../../aspose.words.lowcode/processor/to/#to_3)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | İşlemci için çıkış akışını belirtir. |
| [To](../../aspose.words.lowcode/processor/to/#to_4)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | İşlemci için çıktı dosyasını belirtir. |
| [To](../../aspose.words.lowcode/processor/to/#to_5)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | İşlemci için çıktı dosyasını belirtir. |

## Örnekler

Bağlam kullanılarak tek satır kodla belgelerin nasıl dönüştürüleceğini gösterir.

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

Akıştaki belgeleri kullanarak bir DataTable'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Akıştaki belgeleri kullanarak bir DataTable'dan posta birleştirme işlemi yapmanın birkaç yolu vardır:
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

Bağlam kullanılarak tek satır kodla bir akıştan belgelerin nasıl dönüştürüleceğini gösterir.

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

Bağlam kullanılarak belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
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

Bağlam kullanılarak akıştaki belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
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

### Ayrıca bakınız

* ad alanı [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../)
