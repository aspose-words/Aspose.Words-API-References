---
title: CsvDataLoadOptions.Delimiter
linktitle: Delimiter
articleTitle: Delimiter
second_title: .NET için Aspose.Words
description: Verimli veri yüklemesi için sütun sınırlayıcılarını kolayca özelleştirmek üzere CsvDataLoadOptions Delimiter özelliğini keşfedin. Veri yönetiminizi bugün optimize edin!
type: docs
weight: 30
url: /tr/net/aspose.words.reporting/csvdataloadoptions/delimiter/
---
## CsvDataLoadOptions.Delimiter property

Sütun sınırlayıcı olarak kullanılacak karakteri alır veya ayarlar.

```csharp
public char Delimiter { get; set; }
```

## Notlar

Varsayılan değer ',' (virgül)'dür.

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
