---
title: CsvDataSource
linktitle: CsvDataSource
articleTitle: CsvDataSource
second_title: .NET için Aspose.Words
description: CsvDataSource oluşturucumuzla zahmetsizce güçlü bir CSV veri kaynağı oluşturun. Sorunsuz entegrasyon için varsayılan seçeneklerle veri ayrıştırmayı basitleştirin.
type: docs
weight: 10
url: /tr/net/aspose.words.reporting/csvdatasource/csvdatasource/
---
## CsvDataSource(*string*) {#constructor_2}

CSV verilerini ayrıştırmak için varsayılan seçenekleri kullanarak CSV dosyasındaki verilerle yeni bir veri kaynağı oluşturur.

```csharp
public CsvDataSource(string csvPath)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| csvPath | String | Veri kaynağı olarak kullanılacak CSV dosyasının yolu. |

### Ayrıca bakınız

* class [CsvDataSource](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)

---

## CsvDataSource(*string, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_3}

CSV verilerini ayrıştırmak için belirtilen seçenekleri kullanarak CSV dosyasındaki verilerle yeni bir veri kaynağı oluşturur.

```csharp
public CsvDataSource(string csvPath, CsvDataLoadOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| csvPath | String | Veri kaynağı olarak kullanılacak CSV dosyasının yolu. |
| options | CsvDataLoadOptions | CSV verilerini ayrıştırma seçenekleri. |

## Örnekler

CSV'nin veri kaynağı (dize) olarak nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';
loadOptions.HasHeaders = true;
loadOptions.QuoteChar = '"';

CsvDataSource dataSource = new CsvDataSource(MyDir + "List of people.csv", loadOptions);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataString.docx");
```

### Ayrıca bakınız

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)

---

## CsvDataSource(*Stream*) {#constructor}

CSV verilerini ayrıştırmak için varsayılan seçenekleri kullanarak CSV akışından gelen verilerle yeni bir veri kaynağı oluşturur.

```csharp
public CsvDataSource(Stream csvStream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| csvStream | Stream | Veri kaynağı olarak kullanılacak CSV veri akışı. |

### Ayrıca bakınız

* class [CsvDataSource](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)

---

## CsvDataSource(*Stream, [CsvDataLoadOptions](../../csvdataloadoptions/)*) {#constructor_1}

CSV verilerini ayrıştırmak için belirtilen seçenekleri kullanarak CSV akışından gelen verilerle yeni bir veri kaynağı oluşturur.

```csharp
public CsvDataSource(Stream csvStream, CsvDataLoadOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| csvStream | Stream | Veri kaynağı olarak kullanılacak CSV veri akışı. |
| options | CsvDataLoadOptions | CSV verilerini ayrıştırma seçenekleri. |

## Örnekler

CSV'nin veri kaynağı (akış) olarak nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - CSV data destination.docx");

CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
loadOptions.Delimiter = ';';
loadOptions.CommentChar = '$';

using (FileStream stream = File.OpenRead(MyDir + "List of people.csv"))
{
    CsvDataSource dataSource = new CsvDataSource(stream, loadOptions);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.CsvDataStream.docx");
```

### Ayrıca bakınız

* class [CsvDataLoadOptions](../../csvdataloadoptions/)
* class [CsvDataSource](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)
