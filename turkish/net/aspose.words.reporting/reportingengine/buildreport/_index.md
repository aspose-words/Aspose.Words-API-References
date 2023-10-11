---
title: ReportingEngine.BuildReport
second_title: Aspose.Words for .NET API Referansı
description: ReportingEngine yöntem. Belirtilen şablon belgesini belirtilen kaynaktan gelen verilerle doldurarak onu hazır bir rapor haline getirir.
type: docs
weight: 40
url: /tr/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(Document, object) {#buildreport}

Belirtilen şablon belgesini, belirtilen kaynaktan gelen verilerle doldurarak onu hazır bir rapor haline getirir.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| document | Document | Verilerle doldurulacak bir şablon belge. |
| dataSource | Object | Bir veri kaynağı nesnesi. |

### Geri dönüş değeri

Şablon belgesinin ayrıştırılmasının başarılı olup olmadığını gösteren bir işaret. Döndürülen işaret, yalnızca[`Options`](../options/)özellik 'yi içerirInlineErrorMessages seçenek.

### Notlar

Bu aşırı yüklemeyi kullanarak, şablon belgedeki veri kaynağının üyelerine başvuruda bulunabilirsiniz, ancak veri kaynağı nesnesinin kendisine başvuruda bulunamazsınız. Şunu kullanmalısın:`BuildReport` Bunu başarmak için aşırı yük.

Bir veri kaynağı nesnesi aşağıdaki türlerden birinde olabilir:

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
* Diğer herhangi bir dinamik olmayan ve anonim olmayan .NET type

Şablon belgelerinde farklı türdeki veri kaynaklarıyla nasıl çalışılacağı hakkında bilgi için şablon sözdizimine bakın referansı (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* ad alanı [Aspose.Words.Reporting](../../reportingengine/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(Document, object, string) {#buildreport_1}

Belirtilen şablon belgesini, belirtilen kaynaktan gelen verilerle doldurarak onu hazır bir rapor haline getirir.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| document | Document | Verilerle doldurulacak bir şablon belge. |
| dataSource | Object | Bir veri kaynağı nesnesi. |
| dataSourceName | String | Şablondaki veri kaynağı nesnesine başvuruda bulunacak bir ad. |

### Geri dönüş değeri

Şablon belgesinin ayrıştırılmasının başarılı olup olmadığını gösteren bir işaret. Döndürülen işaret, yalnızca[`Options`](../options/)özellik 'yi içerirInlineErrorMessages seçenek.

### Notlar

Bu aşırı yüklemeyi kullanarak, şablondaki veri kaynağının üyelerine ve veri kaynağı nesnesinin kendisine başvurabilirsiniz. Veri kaynağı nesnesinin kendisine referans vermeyecekseniz, atlayabilirsiniz*dataSourceName* geçiyor`hükümsüz` veya şunu kullanın`BuildReport` aşırı yük.

Bir veri kaynağı nesnesi aşağıdaki türlerden birinde olabilir:

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
* Diğer herhangi bir dinamik olmayan ve anonim olmayan .NET type

Şablon belgelerinde farklı türdeki veri kaynaklarıyla nasıl çalışılacağı hakkında bilgi için şablon sözdizimine bakın referansı (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* ad alanı [Aspose.Words.Reporting](../../reportingengine/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(Document, object[], string[]) {#buildreport_2}

Belirtilen şablon belgeyi, belirtilen kaynaklardan alınan verilerle doldurarak onu hazır bir rapor haline getirir.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| document | Document | Verilerle doldurulacak bir şablon belge. |
| dataSources | Object[] | Bir dizi veri kaynağı nesnesi. |
| dataSourceNames | String[] | Şablon içindeki veri kaynağı nesnelerine başvuruda bulunacak bir ad dizisi. |

### Geri dönüş değeri

Şablon belgesinin ayrıştırılmasının başarılı olup olmadığını gösteren bir işaret. Döndürülen işaret, yalnızca[`Options`](../options/)özellik 'yi içerirInlineErrorMessages seçenek.

### Notlar

Bu aşırı yüklemeyi kullanarak, şablondaki birden çok veri kaynağı nesnesine ve bunların üyelerine başvuruda bulunabilirsiniz. İlk veri kaynağının adı ihmal edilebilir (örn. boş bir dize veya`hükümsüz` veri kaynağı nesnesinin kendisine değil, veri kaynağının üyelerine referans verecekseniz. Diğer veri kaynaklarının adları belirtilmeli ve benzersiz olmalıdır.

Tek bir veri kaynağı kullanacaksanız şunları kullanmayı düşünün:`BuildReport` ve`BuildReport` bunun yerine aşırı yükleniyor.

Bir veri kaynağı nesnesi aşağıdaki türlerden birinde olabilir:

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
* Diğer herhangi bir dinamik olmayan ve anonim olmayan .NET type

Şablon belgelerinde farklı türdeki veri kaynaklarıyla nasıl çalışılacağı hakkında bilgi için şablon sözdizimine bakın referansı (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* ad alanı [Aspose.Words.Reporting](../../reportingengine/)
* toplantı [Aspose.Words](../../../)


