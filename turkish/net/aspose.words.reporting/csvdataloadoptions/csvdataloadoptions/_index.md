---
title: CsvDataLoadOptions
linktitle: CsvDataLoadOptions
articleTitle: CsvDataLoadOptions
second_title: .NET için Aspose.Words
description: CsvDataLoadOptions oluşturucusunu keşfedin; verimli veri yükleme ve sorunsuz entegrasyon için varsayılan ayarlarla kolayca başlatın.
type: docs
weight: 10
url: /tr/net/aspose.words.reporting/csvdataloadoptions/csvdataloadoptions/
---
## CsvDataLoadOptions() {#constructor}

Bu sınıfın yeni bir örneğini varsayılan seçeneklerle başlatır.

```csharp
public CsvDataLoadOptions()
```

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

* class [CsvDataLoadOptions](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)

---

## CsvDataLoadOptions(*bool*) {#constructor_1}

CSV verilerinin ilk satırda sütun adlarını içerip içermediğini belirterek bu sınıfın yeni bir örneğini başlatır.

```csharp
public CsvDataLoadOptions(bool hasHeaders)
```

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

* class [CsvDataLoadOptions](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)
