---
title: ReportBuilder.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: .NET için Aspose.Words
description: ReportBuilder'ın BuildReport yöntemi ile özelleştirilmiş raporları zahmetsizce oluşturun; şablonunuzu verilerle doldurarak her seferinde profesyonel sonuçlar elde edin.
type: docs
weight: 20
url: /tr/net/aspose.words.lowcode/reportbuilder/buildreport/
---
## BuildReport(*string, string, object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_12}

Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve ek seçeneklerle tamamlanmış bir rapor oluşturur.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, object data, 
    ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| data | Object | Bir veri kaynağı nesnesi. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Belgenin verilerle nasıl doldurulacağını gösterir.

```csharp
public void BuildReportData()
{
    // Belgeyi verilerle doldurmanın birkaç yolu vardır:
    string doc = MyDir + "Reporting engine template - If greedy.docx";

    AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.1.docx", obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.2.docx", obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.3.docx", SaveFormat.Docx, obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.4.docx", SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}

public class AsposeData
{
    public List<string> List { get; set; }
}
```

### Ayrıca bakınız

* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveFormat](../../../aspose.words/saveformat/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_6}

Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve belirtilen çıktı biçimi ve ek seçeneklerle tamamlanmış bir rapor oluşturur.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveFormat | SaveFormat | Çıktının kaydedileceği format. |
| data | Object | Bir veri kaynağı nesnesi. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

## Örnekler

Belgenin verilerle nasıl doldurulacağını gösterir.

```csharp
public void BuildReportData()
{
    // Belgeyi verilerle doldurmanın birkaç yolu vardır:
    string doc = MyDir + "Reporting engine template - If greedy.docx";

    AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.1.docx", obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.2.docx", obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.3.docx", SaveFormat.Docx, obj);
    ReportBuilder.BuildReport(doc, ArtifactsDir + "LowCode.BuildReportWithObject.4.docx", SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}

public class AsposeData
{
    public List<string> List { get; set; }
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_9}

Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve belirtilen çıktı biçimi ve ek seçeneklerle tamamlanmış bir rapor oluşturur.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveOptions | SaveOptions | Çıktının kaydetme seçenekleri. |
| data | Object | Bir veri kaynağı nesnesi. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport}

Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve giriş ve çıkış akışlarından belirtilen çıktı biçimi ve ek seçeneklerle tamamlanmış bir rapor oluşturur.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| outputStream | Stream | Çıktı dosya akışı. |
| saveFormat | SaveFormat | Çıktının kaydedileceği format. |
| data | Object | Bir veri kaynağı nesnesi. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Örnekler

Akıştaki belgeleri kullanarak belgenin verilerle nasıl doldurulacağını gösterir.

```csharp
// Akıştaki belgeleri kullanarak belgeyi verilerle doldurmanın birkaç yolu vardır:
AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

using (FileStream streamIn = new FileStream(MyDir + "Reporting engine template - If greedy.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, obj);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_3}

Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve giriş ve çıkış akışlarından belirtilen çıktı biçimi ve ek seçeneklerle tamamlanmış bir rapor oluşturur.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    object data, ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| outputStream | Stream | Çıktı dosya akışı. |
| saveOptions | SaveOptions | Çıktının kaydetme seçenekleri. |
| data | Object | Bir veri kaynağı nesnesi. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(*string, string, object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_13}

Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve adlandırılmış bir veri kaynağı referansı ve ek seçenekler içeren tamamlanmış bir rapor oluşturur.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, object data, 
    string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| data | Object | Bir veri kaynağı nesnesi. |
| dataSourceName | String | Şablondaki veri kaynağı nesnesine başvurmak için bir ad. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

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

* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveFormat](../../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_7}

Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve belirtilen çıktı biçimi, adlandırılmış bir veri kaynağı referansı ve ek seçeneklerle tamamlanmış bir rapor oluşturur.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    object data, string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveFormat | SaveFormat | Çıktının kaydedileceği format. |
| data | Object | Bir veri kaynağı nesnesi. |
| dataSourceName | String | Şablondaki veri kaynağı nesnesine başvurmak için bir ad. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_10}

Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve belirtilen çıktı biçimi, adlandırılmış bir veri kaynağı referansı ve ek seçeneklerle tamamlanmış bir rapor oluşturur.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, object data, string dataSourceName, 
    ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveOptions | SaveOptions | Çıktının kaydetme seçenekleri. |
| data | Object | Bir veri kaynağı nesnesi. |
| dataSourceName | String | Şablondaki veri kaynağı nesnesine başvurmak için bir ad. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_1}

Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve adlandırılmış bir veri kaynağı referansı ve ek seçenekler içeren tamamlanmış bir rapor oluşturur.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    object data, string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| outputStream | Stream | Çıktı dosya akışı. |
| saveFormat | SaveFormat | Çıktının kaydedileceği format. |
| data | Object | Bir veri kaynağı nesnesi. |
| dataSourceName | String | Şablondaki veri kaynağı nesnesine başvurmak için bir ad. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_4}

Şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve adlandırılmış bir veri kaynağı referansı ve ek seçenekler içeren tamamlanmış bir rapor oluşturur.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    object data, string dataSourceName, ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| outputStream | Stream | Çıktı dosya akışı. |
| saveOptions | SaveOptions | Çıktının kaydetme seçenekleri. |
| data | Object | Bir veri kaynağı nesnesi. |
| dataSourceName | String | Şablondaki veri kaynağı nesnesine başvurmak için bir ad. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(*string, string, object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_14}

Şablon belgesini birden fazla kaynaktan gelen verilerle doldurur ve ek seçeneklerle tamamlanmış bir rapor oluşturur. Bu aşırı yükleme, çıktı dosyası uzantısına göre kaydetme biçimini otomatik olarak belirler.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, object[] data, 
    string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| data | Object[] | Veri kaynağı nesnelerinin dizisi. |
| dataSourceNames | String[] | Şablon içindeki veri kaynağı nesnelerine başvurmak için bir ad dizisi. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

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

* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveFormat](../../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_8}

Şablon belgesini birden fazla kaynaktan gelen verilerle doldurur ve belirtilen çıktı biçimi ve ek seçeneklerle tamamlanmış bir rapor oluşturur.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveFormat | SaveFormat | Çıktının kaydedileceği format. |
| data | Object[] | Veri kaynağı nesnelerinin dizisi. |
| dataSourceNames | String[] | Şablon içindeki veri kaynağı nesnelerine başvurmak için bir ad dizisi. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_11}

Şablon belgesini birden fazla kaynaktan gelen verilerle doldurur ve belirtilen çıktı biçimi ve ek seçeneklerle tamamlanmış bir rapor oluşturur.

```csharp
public static void BuildReport(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, object[] data, string[] dataSourceNames, 
    ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputFileName | String | Giriş dosya adı. |
| outputFileName | String | Çıktı dosyasının adı. |
| saveOptions | SaveOptions | Çıktının kaydetme seçenekleri. |
| data | Object[] | Veri kaynağı nesnelerinin dizisi. |
| dataSourceNames | String[] | Şablon içindeki veri kaynağı nesnelerine başvurmak için bir ad dizisi. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Notlar

Çıktı biçimi bir görüntü ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, şu kurala göre her parça için dosya adları oluşturmak için kullanılır: outputFile_partIndex.extension.

Çıkış biçimi TIFF ise, çıkış tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_2}

Şablon belgesini birden fazla kaynaktan gelen verilerle doldurur, belirtilen çıktı biçimi ve belirtilen giriş ve çıkış dosya akışlarından ek seçeneklerle tamamlanmış bir rapor oluşturur.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| outputStream | Stream | Çıktı dosya akışı. |
| saveFormat | SaveFormat | Çıktının kaydedileceği format. |
| data | Object[] | Veri kaynağı nesnelerinin dizisi. |
| dataSourceNames | String[] | Şablon içindeki veri kaynağı nesnelerine başvurmak için bir ad dizisi. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

## Örnekler

Akıştaki belgeleri kullanarak belgenin verilerle nasıl doldurulacağını gösterir.

```csharp
// Akıştaki belgeleri kullanarak belgeyi verilerle doldurmanın birkaç yolu vardır:
AsposeData obj = new AsposeData { List = new List<string> { "abc" } };

using (FileStream streamIn = new FileStream(MyDir + "Reporting engine template - If greedy.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, obj);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, obj, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });

    MessageTestClass sender = new MessageTestClass("LINQ Reporting Engine", "Hello World");
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.BuildReportDataStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        ReportBuilder.BuildReport(streamIn, streamOut, SaveFormat.Docx, new object[] { sender }, new[] { "s" }, new ReportBuilderOptions() { Options = ReportBuildOptions.AllowMissingMembers });
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../../reportbuilderoptions/)*) {#buildreport_5}

Şablon belgesini birden fazla kaynaktan gelen verilerle doldurur, belirtilen çıktı biçimi ve belirtilen giriş ve çıkış dosya akışlarından ek seçeneklerle tamamlanmış bir rapor oluşturur.

```csharp
public static void BuildReport(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    object[] data, string[] dataSourceNames, ReportBuilderOptions reportBuilderOptions = null)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| inputStream | Stream | Giriş dosya akışı. |
| outputStream | Stream | Çıktı dosya akışı. |
| saveOptions | SaveOptions | Çıktının kaydetme seçenekleri. |
| data | Object[] | Veri kaynağı nesnelerinin dizisi. |
| dataSourceNames | String[] | Şablon içindeki veri kaynağı nesnelerine başvurmak için bir ad dizisi. |
| reportBuilderOptions | ReportBuilderOptions | Ek rapor oluşturma seçenekleri. |

## Notlar

Çıkış biçimi bir resim ise (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP), belirtilen akışa yalnızca çıkışın ilk sayfası kaydedilir.

Çıkış biçimi TIFF ise, çıkış belirtilen akışa tek bir çok çerçeveli TIFF olarak kaydedilir.

### Ayrıca bakınız

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [ReportBuilderOptions](../../reportbuilderoptions/)
* class [ReportBuilder](../)
* ad alanı [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../../)
