---
title: "CsvDataSource"
linktitle: "CsvDataSource"
second_title: "Aspose.Words Java için"
description: "Java'da bir rapor içinde kullanılacak CSV dosyası veya akışının verilerine erişim sağlar."
type: docs
weight: 138
url: /tr/java/com.aspose.words/csvdatasource/
---

**Inheritance:**
java.lang.Object
```
public class CsvDataSource
```

Rapor içinde kullanılmak üzere bir CSV dosyasının veya akışının verilerine erişim sağlar.

Daha fazla bilgi için, [ LINQ Reporting Engine ][LINQ Reporting Engine] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bir rapor oluştururken ilgili dosya veya akışın verilerine erişmek için, bu sınıfın bir örneğini veri kaynağı olarak [ReportingEngine](../../com.aspose.words/reportingengine/) öğelerinden birine geçirin. buildReport aşırı yüklemeleri.

Şablon belgelerinde, bir [CsvDataSource](../../com.aspose.words/csvdatasource/) örneği, sanki bir [DataTable](../../com.aspose.words.net.system.data/datatable/) örneğiymiş gibi aynı şekilde ele alınmalıdır. Daha fazla bilgi için şablon sözdizimi referansına bakın(https://docs.aspose.com/display/wordsjava/Template+Syntax).

Virgülle ayrılmış değerlerin veri tipleri, dize temsilleri üzerinden otomatik olarak belirlenir. Bu nedenle şablon belgelerinde yalnızca dizeler yerine tiplenmiş değerlerle çalışabilirsiniz. Motor, aşağıdaki tipteki değerleri otomatik olarak tanıyabilir:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Veri tiplerinin otomatik tanınmasının çalışması için, virgülle ayrılmış değerlerin dize temsillerinin değişmez kültür ayarları kullanılarak oluşturulması gerektiğini unutmayın.

CSV veri yüklemesinin varsayılan davranışını geçersiz kılmak için, bir [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) örneğini başlatın ve bu sınıfın yapıcısına geçirin.

 **Examples:** 

CSV'yi bir veri kaynağı (dize) olarak nasıl kullanacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [CsvDataSource(String csvPath)](#CsvDataSource-java.lang.String) | CSV verilerini ayrıştırmak için varsayılan seçenekleri kullanarak bir CSV dosyasından veriyle yeni bir veri kaynağı oluşturur. |
| [CsvDataSource(String csvPath, CsvDataLoadOptions options)](#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions) | CSV verilerini ayrıştırmak için belirtilen seçenekleri kullanarak bir CSV dosyasından veriyle yeni bir veri kaynağı oluşturur. |
| [CsvDataSource(InputStream csvStream)](#CsvDataSource-java.io.InputStream) | Bu sınıfın yeni bir örneğini başlatır. |
| [CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)](#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions) | Bu sınıfın yeni bir örneğini başlatır. |
### CsvDataSource(String csvPath) {#CsvDataSource-java.lang.String}
```
public CsvDataSource(String csvPath)
```


CSV verilerini ayrıştırmak için varsayılan seçenekleri kullanarak bir CSV dosyasından veriyle yeni bir veri kaynağı oluşturur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| csvPath | java.lang.String | Veri kaynağı olarak kullanılacak CSV dosyasının yolu. |

### CsvDataSource(String csvPath, CsvDataLoadOptions options) {#CsvDataSource-java.lang.String-com.aspose.words.CsvDataLoadOptions}
```
public CsvDataSource(String csvPath, CsvDataLoadOptions options)
```


CSV verilerini ayrıştırmak için belirtilen seçenekleri kullanarak bir CSV dosyasından veriyle yeni bir veri kaynağı oluşturur.

 **Examples:** 

CSV'yi bir veri kaynağı (dize) olarak nasıl kullanacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - CSV data destination (Java).docx");

 CsvDataLoadOptions loadOptions = new CsvDataLoadOptions(true);
 loadOptions.setDelimiter(';');
 loadOptions.setCommentChar('$');
 loadOptions.hasHeaders(true);
 loadOptions.setQuoteChar('"');

 CsvDataSource dataSource = new CsvDataSource(getMyDir() + "List of people.csv", loadOptions);
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.CsvDataString.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| csvPath | java.lang.String | Veri kaynağı olarak kullanılacak CSV dosyasının yolu. |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) | CSV verilerini ayrıştırma seçenekleri. |

### CsvDataSource(InputStream csvStream) {#CsvDataSource-java.io.InputStream}
```
public CsvDataSource(InputStream csvStream)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |

### CsvDataSource(InputStream csvStream, CsvDataLoadOptions options) {#CsvDataSource-java.io.InputStream-com.aspose.words.CsvDataLoadOptions}
```
public CsvDataSource(InputStream csvStream, CsvDataLoadOptions options)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| csvStream | java.io.InputStream |  |
| options | [CsvDataLoadOptions](../../com.aspose.words/csvdataloadoptions/) |  |

