---
title: JsonDataSource
linktitle: JsonDataSource
articleTitle: JsonDataSource
second_title: .NET için Aspose.Words
description: JsonDataSource oluşturucusu ile JSON dosyalarının sorunsuz entegrasyonunu ve optimize edilmiş veri ayrıştırmasını sağlayarak güçlü bir veri kaynağını zahmetsizce oluşturun.
type: docs
weight: 10
url: /tr/net/aspose.words.reporting/jsondatasource/jsondatasource/
---
## JsonDataSource(*string*) {#constructor_2}

JSON verilerini ayrıştırmak için varsayılan seçenekleri kullanarak bir JSON dosyasındaki verilerle yeni bir veri kaynağı oluşturur.

```csharp
public JsonDataSource(string jsonPath)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| jsonPath | String | Veri kaynağı olarak kullanılacak JSON dosyasının yolu. |

### Ayrıca bakınız

* class [JsonDataSource](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)

---

## JsonDataSource(*Stream*) {#constructor}

JSON verilerini ayrıştırmak için varsayılan seçenekleri kullanarak bir JSON akışından gelen verilerle yeni bir veri kaynağı oluşturur.

```csharp
public JsonDataSource(Stream jsonStream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| jsonStream | Stream | Veri kaynağı olarak kullanılacak JSON veri akışı. |

### Ayrıca bakınız

* class [JsonDataSource](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)

---

## JsonDataSource(*string, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_3}

JSON verilerini ayrıştırmak için belirtilen seçenekleri kullanarak bir JSON dosyasından gelen verilerle yeni bir veri kaynağı oluşturur.

```csharp
public JsonDataSource(string jsonPath, JsonDataLoadOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| jsonPath | String | Veri kaynağı olarak kullanılacak JSON dosyasının yolu. |
| options | JsonDataLoadOptions | JSON verilerini ayrıştırma seçenekleri. |

## Örnekler

JSON'un veri kaynağı (dize) olarak nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - JSON data destination.docx");

JsonDataLoadOptions options = new JsonDataLoadOptions
{
    ExactDateTimeParseFormats = new List<string> {"MM/dd/yyyy", "MM.d.yy", "MM d yy"},
    AlwaysGenerateRootObject = true,
    PreserveSpaces = true,
    SimpleValueParseMode = JsonSimpleValueParseMode.Loose
};

JsonDataSource dataSource = new JsonDataSource(MyDir + "List of people.json", options);
BuildReport(doc, dataSource, "persons");

doc.Save(ArtifactsDir + "ReportingEngine.JsonDataString.docx");
```

### Ayrıca bakınız

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)

---

## JsonDataSource(*Stream, [JsonDataLoadOptions](../../jsondataloadoptions/)*) {#constructor_1}

JSON verilerini ayrıştırmak için belirtilen seçenekleri kullanarak bir JSON akışından gelen verilerle yeni bir veri kaynağı oluşturur.

```csharp
public JsonDataSource(Stream jsonStream, JsonDataLoadOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| jsonStream | Stream | Veri kaynağı olarak kullanılacak JSON veri akışı. |
| options | JsonDataLoadOptions | JSON verilerini ayrıştırma seçenekleri. |

## Örnekler

JSON'un veri kaynağı (akış) olarak nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - JSON data destination.docx");

JsonDataLoadOptions options = new JsonDataLoadOptions
{
    ExactDateTimeParseFormats = new List<string> {"MM/dd/yyyy", "MM.d.yy", "MM d yy"}
};

using (FileStream stream = File.OpenRead(MyDir + "List of people.json"))
{
    JsonDataSource dataSource = new JsonDataSource(stream, options);
    BuildReport(doc, dataSource, "persons");
}

doc.Save(ArtifactsDir + "ReportingEngine.JsonDataStream.docx");
```

### Ayrıca bakınız

* class [JsonDataLoadOptions](../../jsondataloadoptions/)
* class [JsonDataSource](../)
* ad alanı [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* toplantı [Aspose.Words](../../../)
