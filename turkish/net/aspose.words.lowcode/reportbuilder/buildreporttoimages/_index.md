---
title: ReportBuilder.BuildReportToImages
linktitle: BuildReportToImages
articleTitle: BuildReportToImages
second_title: .NET için Aspose.Words
description: ReportBuilder'ın BuildReportToImages yöntemiyle şablon belgelerinizi zahmetsizce dönüştürün; çeşitli kaynaklardan gelen verileri birleştirerek çarpıcı görsellere dönüştürün.
type: docs
weight: 30
url: /tr/net/aspose.words.lowcode/reportbuilder/buildreporttoimages/
---
## BuildReportToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreporttoimages_1}

Şablon belgesini birden fazla kaynaktan gelen verilerle doldurur. Çıktıyı resimlere dönüştürür.

```csharp
public static Stream[] BuildReportToImages(string inputFileName, ImageSaveOptions saveOptions, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| saveOptions | ImageSaveOptions | Çıktının kaydetme seçenekleri. |
| data | Object[] | Veri kaynağı nesnelerinin dizisi. |
| dataSourceNames | String[] | Şablon içindeki veri kaynağı nesnelerine başvurmak için bir ad dizisi. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Örnekler

Belgenin veri kaynaklarıyla nasıl doldurulacağını gösterir.

```csharp
public void BuildReportDataSource()
{
    // Belgeyi veri kaynaklarıyla doldurmanın birkaç yolu vardır:
    string doc = MyDir + "Report building.docx";

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.1.docx", sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.2.docx", new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.3.docx", sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.4.docx", SaveFormat.Docx, sender, "s");
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.5.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.6.docx", SaveFormat.Docx, sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.7.docx", SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportDataSource.8.docx", new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    Stream[] images = ReportBuilder.BuildReportToImages(doc, new ImageSaveOptions(SaveFormat.Png), new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
    reportBuilderContext.ReportBuilderOptions.MissingMemberMessage = "Missed members";
    reportBuilderContext.DataSources.Add(sender, "s");

    ReportBuilder.Create(reportBuilderContext)
        .From(doc)
        .To(ArtifactsDir + "LowCode.BuildReportDataSource.9.docx")
        .Execute();
}

public class MessageTestClass
{
    public string Name { get; set; }
    public string Message { get; set; }

    public MessageTestClass(string name, string message)
    {
        Name = name;
        Message = message;
    }
}
```

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## BuildReportToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreporttoimages}

Şablon belgesini birden fazla kaynaktan gelen verilerle doldurur. Çıktıyı resimlere dönüştürür.

```csharp
public static Stream[] BuildReportToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| saveOptions | ImageSaveOptions | Çıktının kaydetme seçenekleri. |
| data | Object[] | Veri kaynağı nesnelerinin dizisi. |
| dataSourceNames | String[] | Şablon içindeki veri kaynağı nesnelerine başvurmak için bir ad dizisi. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Örnekler

Akıştaki belgeleri kullanarak belgenin veri kaynaklarıyla nasıl doldurulacağını gösterir.

```csharp
// Akıştaki belgeleri kullanarak belgeyi veri kaynaklarıyla doldurmanın birkaç yolu vardır:
MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");

using (FileStream streamIn = new FileStream(MyDir + "Report building.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, new object[] { sender }, new[] { "s" });

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, sender, "s");

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, sender, "s", new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    Stream[] images = ReportBuilder.BuildReportToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    ReportBuilderContext reportBuilderContext = new ReportBuilderContext();
    reportBuilderContext.ReportBuilderOptions.MissingMemberMessage = "Missed members";
    reportBuilderContext.DataSources.Add(sender, "s");

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataSourceStream.4.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.Create(reportBuilderContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Ayrıca bakınız

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
