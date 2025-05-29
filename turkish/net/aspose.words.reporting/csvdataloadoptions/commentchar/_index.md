---
title: CsvDataLoadOptions.CommentChar
linktitle: CommentChar
articleTitle: CommentChar
second_title: .NET için Aspose.Words
description: CSV veri işlemenizi geliştirmek için CsvDataLoadOptions'daki CommentChar özelliğini nasıl özelleştireceğinizi keşfedin. Veri yüklemenizi bugün optimize edin!
type: docs
weight: 20
url: /tr/net/aspose.words.reporting/csvdataloadoptions/commentchar/
---
## CsvDataLoadOptions.CommentChar property

CSV verilerinin satırlarını yorumlamak için kullanılan karakteri alır veya ayarlar.

```csharp
public char CommentChar { get; set; }
```

## Notlar

Varsayılan değer '#' (sayı işareti)'dir.

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
