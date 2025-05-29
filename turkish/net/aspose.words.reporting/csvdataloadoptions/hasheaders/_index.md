---
title: CsvDataLoadOptions.HasHeaders
linktitle: HasHeaders
articleTitle: HasHeaders
second_title: .NET için Aspose.Words
description: Sorunsuz veri entegrasyonu için ilk kaydın sütun adlarını içerip içermediğini belirterek CSV içe aktarımlarını kolayca yönetmek için CsvDataLoadOptions'ın HasHeaders özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.reporting/csvdataloadoptions/hasheaders/
---
## CsvDataLoadOptions.HasHeaders property

CSV verilerinin ilk kaydının sütun adlarını içerip içermediğini belirten bir değeri alır veya ayarlar.

```csharp
public bool HasHeaders { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` .

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
