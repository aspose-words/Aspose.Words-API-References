---
title: BuildReport
second_title: Aspose.Words for .NET API Referansı
description: Belirtilen şablon belgesini belirtilen kaynaktan alınan verilerle doldurarak hazır bir rapor haline getirir.
type: docs
weight: 40
url: /tr/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(Document, object) {#buildreport}

Belirtilen şablon belgesini, belirtilen kaynaktan alınan verilerle doldurarak hazır bir rapor haline getirir.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| document | Document | Verilerle doldurulacak bir şablon belge. |
| dataSource | Object | Bir veri kaynağı nesnesi. |

### Geri dönüş değeri

Şablon belgesinin ayrıştırılmasının başarılı olup olmadığını gösteren bir bayrak. Döndürülen bayrak, yalnızca[`Options`](../options/)özellik şunları içerir: InlineErrorMessages seçenek.

### Notlar

Bu aşırı yüklemeyi kullanarak şablon belgesinde veri kaynağının üyelerine başvurabilirsiniz, ancak veri kaynağı nesnesinin kendisine başvuramazsınız. kullanmalısın`BuildReport` bunu başarmak için aşırı yükleme.

Bir veri kaynağı nesnesi aşağıdaki türlerden biri olabilir:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Herhangi bir isteğe bağlı dinamik olmayan ve anonim olmayan .NET type

Şablon belgelerinde farklı türlerdeki veri kaynaklarıyla nasıl çalışılacağı hakkında bilgi için, bkz. şablon sözdizimi referansı (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* ad alanı [Aspose.Words.Reporting](../../reportingengine/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(Document, object, string) {#buildreport_1}

Belirtilen şablon belgesini, belirtilen kaynaktan alınan verilerle doldurarak hazır bir rapor haline getirir.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| document | Document | Verilerle doldurulacak bir şablon belge. |
| dataSource | Object | Bir veri kaynağı nesnesi. |
| dataSourceName | String | Şablondaki veri kaynağı nesnesine başvurulacak bir ad. |

### Geri dönüş değeri

Şablon belgesinin ayrıştırılmasının başarılı olup olmadığını gösteren bir bayrak. Döndürülen bayrak, yalnızca[`Options`](../options/)özellik şunları içerir: InlineErrorMessages seçenek.

### Notlar

Bu aşırı yüklemeyi kullanarak, şablonda veri kaynağının üyelerine ve veri kaynağı nesnesinin kendisine başvurabilirsiniz. Veri kaynağı nesnesinin kendisine başvurmayacaksanız, atlayabilirsiniz*dataSourceName* null değerini geçer veya`BuildReport` aşırı yük.

Bir veri kaynağı nesnesi aşağıdaki türlerden biri olabilir:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Herhangi bir isteğe bağlı dinamik olmayan ve anonim olmayan .NET type

Şablon belgelerinde farklı türlerdeki veri kaynaklarıyla nasıl çalışılacağı hakkında bilgi için, bkz. şablon sözdizimi referansı (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* ad alanı [Aspose.Words.Reporting](../../reportingengine/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(Document, object[], string[]) {#buildreport_2}

Belirtilen şablon belgesini, belirtilen kaynaklardan alınan verilerle doldurarak hazır bir rapor haline getirir.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| document | Document | Verilerle doldurulacak bir şablon belge. |
| dataSources | Object[] | Bir dizi veri kaynağı nesnesi. |
| dataSourceNames | String[] | Şablon içindeki veri kaynağı nesnelerine başvurulacak bir ad dizisi. |

### Geri dönüş değeri

Şablon belgesinin ayrıştırılmasının başarılı olup olmadığını gösteren bir bayrak. Döndürülen bayrak, yalnızca[`Options`](../options/)özellik şunları içerir: InlineErrorMessages seçenek.

### Notlar

Bu aşırı yüklemeyi kullanarak, şablonda birden çok veri kaynağı nesnesine ve bunların üyelerine başvurabilirsiniz. Veri kaynağının üyelerine başvuruda bulunacak ancak veri kaynağı nesnesinin kendisine değil başvuru yapacaksanız, ilk veri kaynağının adı atlanabilir (yani boş bir dize veya boş olabilir). Diğer veri kaynaklarının adları belirtilmiş ve benzersiz olmalıdır.

Tek bir veri kaynağı kullanacaksanız, şunu kullanmayı düşünün:`BuildReport` ve`BuildReport` bunun yerine aşırı yükler.

Bir veri kaynağı nesnesi aşağıdaki türlerden biri olabilir:

* [`XmlDataSource`](../../xmldatasource/)
* [`JsonDataSource`](../../jsondatasource/)
* [`CsvDataSource`](../../csvdatasource/)
* DataSet
* DataTable
* DataRow
* IDataReader
* IDataRecord
* DataView
* DataRowView
* Herhangi bir isteğe bağlı dinamik olmayan ve anonim olmayan .NET type

Şablon belgelerinde farklı türlerdeki veri kaynaklarıyla nasıl çalışılacağı hakkında bilgi için, bkz. şablon sözdizimi referansı (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* ad alanı [Aspose.Words.Reporting](../../reportingengine/)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
