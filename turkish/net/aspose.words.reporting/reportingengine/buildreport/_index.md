---
title: ReportingEngine.BuildReport
linktitle: BuildReport
articleTitle: BuildReport
second_title: .NET için Aspose.Words
description: ReportingEngine'in BuildReport yöntemi ile hazır kullanıma hazır raporları zahmetsizce oluşturun; şablonları seçtiğiniz kaynaktan gelen verilerle sorunsuz bir şekilde doldurun.
type: docs
weight: 50
url: /tr/net/aspose.words.reporting/reportingengine/buildreport/
---
## BuildReport(*[Document](../../../aspose.words/document/), object*) {#buildreport}

Belirtilen şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve onu hazır bir rapor haline getirir.

```csharp
public bool BuildReport(Document document, object dataSource)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| document | Document | Verilerle doldurulacak bir şablon belge. |
| dataSource | Object | Bir veri kaynağı nesnesi. |

### Geri dönüş değeri

Şablon belgesinin ayrıştırılmasının başarılı olup olmadığını belirten bir bayrak. Döndürülen bayrak yalnızca bir değer varsa anlamlıdır.[`Options`](../options/) mülk içerirInlineErrorMessages seçenek.

## Notlar

Bu aşırı yüklemeyi kullanarak şablon belgesindeki veri kaynağının üyelerine başvurabilirsiniz, ancak veri kaynağı nesnesinin kendisine başvuramazsınız.`BuildReport` Bunu başarmak için aşırı yüklemesi yapın.

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
* Herhangi bir diğer keyfi dinamik olmayan ve anonim olmayan .NET türü

Şablon belgelerinde farklı türlerdeki veri kaynaklarıyla nasıl çalışılacağı hakkında bilgi için şablon sözdizimi başvurusuna bakın (https://docs.aspose.com/display/wordsnet/Template+Syntax).

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object, string*) {#buildreport_1}

Belirtilen şablon belgesini belirtilen kaynaktan gelen verilerle doldurur ve onu hazır bir rapor haline getirir.

```csharp
public bool BuildReport(Document document, object dataSource, string dataSourceName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| document | Document | Verilerle doldurulacak bir şablon belge. |
| dataSource | Object | Bir veri kaynağı nesnesi. |
| dataSourceName | String | Şablondaki veri kaynağı nesnesine başvurmak için bir ad. |

### Geri dönüş değeri

Şablon belgesinin ayrıştırılmasının başarılı olup olmadığını belirten bir bayrak. Döndürülen bayrak yalnızca bir değer varsa anlamlıdır.[`Options`](../options/) mülk içerirInlineErrorMessages seçenek.

## Notlar

Bu aşırı yüklemeyi kullanarak şablondaki veri kaynağının üyelerine ve veri kaynağı nesnesinin kendisine başvurabilirsiniz. Veri kaynağı nesnesinin kendisine başvurmayacaksanız, bunu atlayabilirsiniz*dataSourceName* geçiyor`hükümsüz` veya kullanın`BuildReport` aşırı yükleme.

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
* Herhangi bir diğer keyfi dinamik olmayan ve anonim olmayan .NET türü

Şablon belgelerinde farklı türlerdeki veri kaynaklarıyla nasıl çalışılacağı hakkında bilgi için şablon sözdizimi başvurusuna bakın (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## Örnekler

Eksik üyelere nasıl izin verileceğini gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();
builder.Writeln("<<[missingObject.First().id]>>");
builder.Writeln("<<foreach [in missingObject]>><<[id]>><</foreach>>");

ReportingEngine engine = new ReportingEngine { Options = ReportBuildOptions.AllowMissingMembers };
engine.MissingMemberMessage = "Missed";
engine.BuildReport(builder.Document, new DataSet(), "");
```

Paragrafların seçici olarak nasıl kaldırılacağını gösterir.

```csharp
// Şablon ünlem işareti içeren etiketler içeriyor. Bu tür etiketler için boş paragraflar kaldırılacak.
Document doc = new Document(MyDir + "Reporting engine template - Selective remove paragraphs.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, false, "value");

doc.Save(ArtifactsDir + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
```

Değerlerin dolar metni olarak nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("<<[ds.Value1]:dollarText>>\r<<[ds.Value2]:dollarText>>");

NumericTestClass testData = new NumericTestBuilder().WithValues(1234, 5621718.589).Build();

ReportingEngine report = new ReportingEngine();
report.KnownTypes.Add(typeof(NumericTestClass));
report.BuildReport(doc, testData, "ds");

doc.Save(ArtifactsDir + "ReportingEngine.DollarTextFormat.docx");
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)

---

## BuildReport(*[Document](../../../aspose.words/document/), object[], string[]*) {#buildreport_2}

Belirtilen şablon belgesini belirtilen kaynaklardan gelen verilerle doldurarak hazır bir rapor haline getirir.

```csharp
public bool BuildReport(Document document, object[] dataSources, string[] dataSourceNames)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| document | Document | Verilerle doldurulacak bir şablon belge. |
| dataSources | Object[] | Veri kaynağı nesnelerinin dizisi. |
| dataSourceNames | String[] | Şablon içindeki veri kaynağı nesnelerine başvurmak için bir ad dizisi. |

### Geri dönüş değeri

Şablon belgesinin ayrıştırılmasının başarılı olup olmadığını belirten bir bayrak. Döndürülen bayrak yalnızca bir değer varsa anlamlıdır.[`Options`](../options/) mülk içerirInlineErrorMessages seçenek.

## Notlar

Bu aşırı yüklemeyi kullanarak şablondaki birden fazla veri kaynağı nesnesine ve üyelerine başvurabilirsiniz. İlk veri kaynağının adı atlanabilir (yani boş bir dize olabilir veya`hükümsüz` yapacaksanız veri kaynağının üyelerine başvuruda bulunun ancak veri kaynağı nesnesinin kendisine değil. Diğer veri kaynaklarının adları belirtilmeli ve benzersiz olmalıdır.

Tek bir veri kaynağı kullanacaksanız, şunları kullanmayı düşünün:`BuildReport` ve`BuildReport` bunun yerine aşırı yüklemeler.

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
* Herhangi bir diğer keyfi dinamik olmayan ve anonim olmayan .NET türü

Şablon belgelerinde farklı türlerdeki veri kaynaklarıyla nasıl çalışılacağı hakkında bilgi için şablon sözdizimi başvurusuna bakın (https://docs.aspose.com/display/wordsnet/Template+Syntax).

## Örnekler

Word 2016'daki grafiklerle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Word 2016 Charts.docx");

ReportingEngine engine = new ReportingEngine();
engine.BuildReport(doc, new object[] { Common.GetShares(), Common.GetShareQuotes() },
    new string[] { "shares", "quotes" });

doc.Save(ArtifactsDir + "ReportingEngine.Word2016Charts.docx");
```

Eklenen numaralandırmanın olduğu gibi nasıl korunacağını gösterir.

```csharp
// Varsayılan olarak, bir şablon belgedeki numaralandırılmış listeler, tanımlayıcıları eklenen bir belgedeki tanımlayıcılarla eşleştiğinde devam eder.
// "-sourceNumbering" ile numaralandırma ayrılmalı ve olduğu gibi bırakılmalıdır.
Document template = DocumentHelper.CreateSimpleDocument("<<doc [src.Document]>>" + Environment.NewLine + "<<doc [src.Document] -sourceNumbering>>");

DocumentTestClass doc = new DocumentTestBuilder()
    .WithDocument(new Document(MyDir + "List item.docx")).Build();

ReportingEngine engine = new ReportingEngine() { Options = ReportBuildOptions.RemoveEmptyParagraphs };
engine.BuildReport(template, new object[] { doc }, new[] { "src" });

template.Save(ArtifactsDir + "ReportingEngine.SourseListNumbering.docx");
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [ReportingEngine](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)
