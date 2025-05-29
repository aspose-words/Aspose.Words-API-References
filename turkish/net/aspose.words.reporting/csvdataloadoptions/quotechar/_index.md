---
title: CsvDataLoadOptions.QuoteChar
linktitle: QuoteChar
articleTitle: QuoteChar
second_title: .NET için Aspose.Words
description: Sorunsuz veri işleme ve gelişmiş CSV yönetimi için alan değeri tekliflerini kolayca özelleştirmek amacıyla CsvDataLoadOptions QuoteChar özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.reporting/csvdataloadoptions/quotechar/
---
## CsvDataLoadOptions.QuoteChar property

Alan değerlerini tırnak işaretine eklemek için kullanılan karakteri alır veya ayarlar.

```csharp
public char QuoteChar { get; set; }
```

## Notlar

Varsayılan değer '"' (tırnak işareti)'dir.

Karakteri tırnak içine almak için karakteri iki katına çıkarın.

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
