---
title: CsvDataLoadOptions Class
linktitle: CsvDataLoadOptions
articleTitle: CsvDataLoadOptions
second_title: .NET için Aspose.Words
description: Verimli CSV veri ayrıştırma için Aspose.Words.Reporting.CsvDataLoadOptions'ı keşfedin. Bugün özelleştirilebilir seçeneklerle belge işlemenizi optimize edin!
type: docs
weight: 5400
url: /tr/net/aspose.words.reporting/csvdataloadoptions/
---
## CsvDataLoadOptions class

CSV verilerini ayrıştırma seçeneklerini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[LINQ Raporlama Motoru](https://docs.aspose.com/words/net/linq-reporting-engine/) belgeleme makalesi.

```csharp
public class CsvDataLoadOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor)() | Bu sınıfın yeni bir örneğini varsayılan seçeneklerle başlatır. |
| [CsvDataLoadOptions](csvdataloadoptions/#constructor_1)(*bool*) | CSV verilerinin ilk satırda sütun adlarını içerip içermediğini belirterek bu sınıfın yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CommentChar](../../aspose.words.reporting/csvdataloadoptions/commentchar/) { get; set; } | CSV verilerinin satırlarını yorumlamak için kullanılan karakteri alır veya ayarlar. |
| [Delimiter](../../aspose.words.reporting/csvdataloadoptions/delimiter/) { get; set; } | Sütun sınırlayıcı olarak kullanılacak karakteri alır veya ayarlar. |
| [HasHeaders](../../aspose.words.reporting/csvdataloadoptions/hasheaders/) { get; set; } | CSV verilerinin ilk kaydının sütun adlarını içerip içermediğini belirten bir değeri alır veya ayarlar. |
| [QuoteChar](../../aspose.words.reporting/csvdataloadoptions/quotechar/) { get; set; } | Alan değerlerini tırnak işaretine eklemek için kullanılan karakteri alır veya ayarlar. |

## Notlar

Bu sınıfın bir örneği, kurucularına geçirilebilir[`CsvDataSource`](../csvdatasource/) .

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

* ad alanı [Aspose.Words.Reporting](../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../)
