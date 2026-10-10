---
title: "JsonDataSource"
linktitle: "JsonDataSource"
second_title: "Aspose.Words Java için"
description: "Java'da bir rapor içinde kullanılacak JSON dosyası veya akışının verilerine erişim sağlar."
type: docs
weight: 409
url: /tr/java/com.aspose.words/jsondatasource/
---

**Inheritance:**
java.lang.Object
```
public class JsonDataSource
```

Rapor içinde kullanılacak bir JSON dosyasının veya akışının verilerine erişim sağlar.

Daha fazla bilgi için, [ LINQ Reporting Engine ][LINQ Reporting Engine] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bir rapor oluştururken ilgili dosya veya akışın verilerine erişmek için, bu sınıfın bir örneğini veri kaynağı olarak [ReportingEngine](../../com.aspose.words/reportingengine/) öğelerinden birine geçirin. buildReport aşırı yüklemeleri.

Şablon belgelerinde, üst düzey bir JSON öğesi bir dizi ise, bir [JsonDataSource](../../com.aspose.words/jsondatasource/) örneği, sanki bir [DataTable](../../com.aspose.words.net.system.data/datatable/) örneğiymiş gibi aynı şekilde ele alınmalıdır. Üst düzey bir JSON öğesi bir nesne ise, bir [JsonDataSource](../../com.aspose.words/jsondatasource/) örneği, sanki bir [DataRow](../../com.aspose.words.net.system.data/datarow/) örneğiymiş gibi aynı şekilde ele alınmalıdır. Daha fazla bilgi için şablon sözdizimi referansına(https://docs.aspose.com/display/wordsjava/Template+Syntax) bakın.

Şablon belgelerinde, JSON öğelerinin tiplenmiş değerleriyle çalışabilirsiniz. Kolaylık sağlamak için, motor JSON basit tiplerinin kümesini aşağıdakilerle değiştirir:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Motor, ek tiplerin değerlerini JSON temsilleri üzerinden otomatik olarak tanır.

JSON veri yüklemenin varsayılan davranışını geçersiz kılmak için, bir [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) örneğini başlatın ve bu sınıfın yapıcısına geçirin.

 **Examples:** 

JSON'u bir veri kaynağı (dize) olarak nasıl kullanacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - JSON data destination (Java).docx");

 JsonDataLoadOptions options = new JsonDataLoadOptions();
 {
     options.setExactDateTimeParseFormats(Arrays.asList(new String[]{"MM/dd/yyyy", "MM.d.yy", "MM d yy"}));
 }

 JsonDataSource dataSource = new JsonDataSource(getMyDir() + "List of people.json", options);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.JsonDataString.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [JsonDataSource(String jsonPath)](#JsonDataSource-java.lang.String) | JSON verilerini ayrıştırmak için varsayılan seçenekleri kullanarak bir JSON dosyasından veri ile yeni bir veri kaynağı oluşturur. |
| [JsonDataSource(InputStream jsonStream)](#JsonDataSource-java.io.InputStream) | Bu sınıfın yeni bir örneğini başlatır. |
| [JsonDataSource(String jsonPath, JsonDataLoadOptions options)](#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions) | JSON verilerini ayrıştırmak için belirtilen seçenekleri kullanarak bir JSON dosyasından veri ile yeni bir veri kaynağı oluşturur. |
| [JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)](#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions) | Bu sınıfın yeni bir örneğini başlatır. |
### JsonDataSource(String jsonPath) {#JsonDataSource-java.lang.String}
```
public JsonDataSource(String jsonPath)
```


JSON verilerini ayrıştırmak için varsayılan seçenekleri kullanarak bir JSON dosyasından veri ile yeni bir veri kaynağı oluşturur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| jsonPath | java.lang.String | Veri kaynağı olarak kullanılacak JSON dosyasının yolu. |

### JsonDataSource(InputStream jsonStream) {#JsonDataSource-java.io.InputStream}
```
public JsonDataSource(InputStream jsonStream)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |

### JsonDataSource(String jsonPath, JsonDataLoadOptions options) {#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions}
```
public JsonDataSource(String jsonPath, JsonDataLoadOptions options)
```


JSON verilerini ayrıştırmak için belirtilen seçenekleri kullanarak bir JSON dosyasından veri ile yeni bir veri kaynağı oluşturur.

 **Examples:** 

JSON'u bir veri kaynağı (dize) olarak nasıl kullanacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - JSON data destination (Java).docx");

 JsonDataLoadOptions options = new JsonDataLoadOptions();
 {
     options.setExactDateTimeParseFormats(Arrays.asList(new String[]{"MM/dd/yyyy", "MM.d.yy", "MM d yy"}));
 }

 JsonDataSource dataSource = new JsonDataSource(getMyDir() + "List of people.json", options);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.JsonDataString.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| jsonPath | java.lang.String | Veri kaynağı olarak kullanılacak JSON dosyasının yolu. |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) | JSON verilerini ayrıştırma seçenekleri. |

### JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options) {#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions}
```
public JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions/) |  |

