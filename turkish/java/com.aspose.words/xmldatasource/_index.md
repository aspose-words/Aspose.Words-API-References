---
title: "XmlDataSource"
linktitle: "XmlDataSource"
second_title: "Aspose.Words Java için"
description: "Java'da bir rapor içinde kullanılacak XML dosyası veya akışının verilerine erişim sağlar."
type: docs
weight: 746
url: /tr/java/com.aspose.words/xmldatasource/
---

**Inheritance:**
java.lang.Object
```
public class XmlDataSource
```

Bir rapor içinde kullanılacak bir XML dosyasının veya akışının verilerine erişim sağlar.

Daha fazla bilgi için, [ LINQ Reporting Engine ][LINQ Reporting Engine] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bir rapor oluştururken ilgili dosya veya akışın verilerine erişmek için, bu sınıfın bir örneğini veri kaynağı olarak [ReportingEngine](../../com.aspose.words/reportingengine/) öğelerinden birine geçirin. buildReport aşırı yüklemeleri.

Şablon belgelerinde, üst düzey bir XML öğesi yalnızca aynı tipte öğeler listesi içeriyorsa, bir [XmlDataSource](../../com.aspose.words/xmldatasource/) örneği, sanki bir [DataTable](../../com.aspose.words.net.system.data/datatable/) örneğiymiş gibi aynı şekilde ele alınmalıdır. Aksi takdirde, bir [XmlDataSource](../../com.aspose.words/xmldatasource/) örneği, sanki bir [DataRow](../../com.aspose.words.net.system.data/datarow/) örneğiymiş gibi aynı şekilde ele alınmalıdır. Daha fazla bilgi için şablon sözdizimi referansına bakın(https://docs.aspose.com/display/wordsjava/Template+Syntax).

XML Şema Tanımı bu sınıfın yapıcısına geçirildiğinde, basit XML öğeleri ve özniteliklerinin değerlerinin veri tipleri şemaya göre belirlenir. Böylece şablon belgelerinde yalnızca dize yerine tiplenmiş değerlerle çalışabilirsiniz.

XML Şema Tanımı bu sınıfın yapıcısına geçirilmediğinde, basit XML öğeleri ve özniteliklerinin değerlerinin veri tipleri, dize temsilleri üzerinden otomatik olarak belirlenir. Bu nedenle şablon belgelerinde bu durumda da tiplenmiş değerlerle çalışabilirsiniz. Motor, aşağıdaki tipteki değerleri otomatik olarak tanıyabilir:

 *  long
 *  double
 *  boolean
 *  java.util.Date
 *  java.lang.String

Veri tiplerinin otomatik olarak tanınabilmesi için, basit XML öğeleri ve özniteliklerinin değerlerinin dize temsillerinin değişmez kültür ayarları kullanılarak oluşturulması gerektiğini unutmayın.

XML veri yüklemesinin varsayılan davranışını geçersiz kılmak için, bir [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) örneğini başlatıp bu sınıfın yapıcısına geçirin.

 **Examples:** 

XML'i veri kaynağı (dize) olarak nasıl kullanacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 XmlDataSource dataSource = new XmlDataSource(getMyDir() + "List of people.xml");
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataString.docx");
 
```

XML'i veri kaynağı (akış) olarak nasıl kullanacağınızı gösterin.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 InputStream stream = new FileInputStream(getMyDir() + "List of people.xml");
 try {
     XmlDataSource dataSource = new XmlDataSource(stream);
     buildReport(doc, dataSource, "persons");
 } finally {
     stream.close();
 }

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataStream.docx");
 
```


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [XmlDataSource(String xmlPath)](#XmlDataSource-java.lang.String) | XML veri yükleme için varsayılan seçenekleri kullanarak bir XML dosyasından veri ile yeni bir veri kaynağı oluşturur. |
| [XmlDataSource(InputStream xmlStream)](#XmlDataSource-java.io.InputStream) | Bu sınıfın yeni bir örneğini başlatır. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath)](#XmlDataSource-java.lang.String-java.lang.String) | XML Şema Tanım dosyasını kullanarak bir XML dosyasından veri ile yeni bir veri kaynağı oluşturur. |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)](#XmlDataSource-java.io.InputStream-java.io.InputStream) | Bu sınıfın yeni bir örneğini başlatır. |
| [XmlDataSource(String xmlPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions) | XML veri yükleme için belirtilen seçenekleri kullanarak bir XML dosyasından veri ile yeni bir veri kaynağı oluşturur. |
| [XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions) | Bu sınıfın yeni bir örneğini başlatır. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions) | XML Şema Tanım dosyasını kullanarak bir XML dosyasından veri ile yeni bir veri kaynağı oluşturur. |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions) | Bu sınıfın yeni bir örneğini başlatır. |
### XmlDataSource(String xmlPath) {#XmlDataSource-java.lang.String}
```
public XmlDataSource(String xmlPath)
```


XML veri yükleme için varsayılan seçenekleri kullanarak bir XML dosyasından veri ile yeni bir veri kaynağı oluşturur.

 **Examples:** 

XML'i veri kaynağı (dize) olarak nasıl kullanacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - XML data destination (Java).docx");

 XmlDataSource dataSource = new XmlDataSource(getMyDir() + "List of people.xml");
 buildReport(doc, dataSource, "persons");

 doc.save(getArtifactsDir() + "ReportingEngine.XmlDataString.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xmlPath | java.lang.String | Veri kaynağı olarak kullanılacak XML dosyasının yolu. |

### XmlDataSource(InputStream xmlStream) {#XmlDataSource-java.io.InputStream}
```
public XmlDataSource(InputStream xmlStream)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath) {#XmlDataSource-java.lang.String-java.lang.String}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath)
```


XML Şema Tanım dosyasını kullanarak bir XML dosyasından veri ile yeni bir veri kaynağı oluşturur. XML veri yükleme için varsayılan seçenekler kullanılır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xmlPath | java.lang.String | Veri kaynağı olarak kullanılacak XML dosyasının yolu. |
| xmlSchemaPath | java.lang.String | XML dosyası için şema sağlayan XML Şema Tanım dosyasının yolu. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream) {#XmlDataSource-java.io.InputStream-java.io.InputStream}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(String xmlPath, XmlDataLoadOptions options)
```


XML veri yükleme için belirtilen seçenekleri kullanarak bir XML dosyasından veri ile yeni bir veri kaynağı oluşturur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xmlPath | java.lang.String | Veri kaynağı olarak kullanılacak XML dosyasının yolu. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) | XML veri yükleme seçenekleri. |

### XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)
```


XML Şema Tanım dosyasını kullanarak bir XML dosyasından veri ile yeni bir veri kaynağı oluşturur. Belirtilen seçenekler XML veri yükleme için kullanılır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xmlPath | java.lang.String | Veri kaynağı olarak kullanılacak XML dosyasının yolu. |
| xmlSchemaPath | java.lang.String | XML dosyası için şema sağlayan XML Şema Tanım dosyasının yolu. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) | XML veri yükleme seçenekleri. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)
```


Bu sınıfın yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions/) |  |

