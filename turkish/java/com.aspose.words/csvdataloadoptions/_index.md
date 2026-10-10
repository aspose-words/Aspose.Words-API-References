---
title: "CsvDataLoadOptions"
linktitle: "CsvDataLoadOptions"
second_title: "Aspose.Words Java için"
description: "Java'da CSV verilerini ayrıştırmak için seçenekleri temsil eder."
type: docs
weight: 137
url: /tr/java/com.aspose.words/csvdataloadoptions/
---

**Inheritance:**
java.lang.Object
```
public class CsvDataLoadOptions
```

CSV verilerini ayrıştırma seçeneklerini temsil eder.

Daha fazla bilgi için, [ LINQ Reporting Engine ][LINQ Reporting Engine] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bu sınıfın bir örneği, [CsvDataSource](../../com.aspose.words/csvdatasource/) yapıcılarına geçirilebilir.

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
| [CsvDataLoadOptions()](#CsvDataLoadOptions) | Bu sınıfın yeni bir örneğini varsayılan seçeneklerle başlatır. |
| [CsvDataLoadOptions(boolean hasHeaders)](#CsvDataLoadOptions-boolean) | Bu sınıfın yeni bir örneğini, CSV verilerinin ilk satırda sütun adları içerip içermediğini belirterek başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getCommentChar()](#getCommentChar) | CSV verilerinin satırlarını yorumlamak için kullanılan karakteri alır. |
| [getDelimiter()](#getDelimiter) | Sütun ayırıcı olarak kullanılacak karakteri alır. |
| [getQuoteChar()](#getQuoteChar) | Alan değerlerini tırnak içine almak için kullanılan karakteri alır. |
| [hasHeaders()](#hasHeaders) | CSV verilerinin ilk kaydının sütun adları içerip içermediğini gösteren bir değeri alır. |
| [hasHeaders(boolean value)](#hasHeaders-boolean) | CSV verilerinin ilk kaydının sütun adları içerip içermediğini gösteren bir değeri ayarlar. |
| [setCommentChar(char value)](#setCommentChar-char) | CSV verilerinin satırlarını yorumlamak için kullanılan karakteri ayarlar. |
| [setDelimiter(char value)](#setDelimiter-char) | Sütun ayırıcı olarak kullanılacak karakteri ayarlar. |
| [setQuoteChar(char value)](#setQuoteChar-char) | Alan değerlerini tırnak içine almak için kullanılan karakteri ayarlar. |
### CsvDataLoadOptions() {#CsvDataLoadOptions}
```
public CsvDataLoadOptions()
```


Bu sınıfın yeni bir örneğini varsayılan seçeneklerle başlatır.

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

### CsvDataLoadOptions(boolean hasHeaders) {#CsvDataLoadOptions-boolean}
```
public CsvDataLoadOptions(boolean hasHeaders)
```


Bu sınıfın yeni bir örneğini, CSV verilerinin ilk satırda sütun adları içerip içermediğini belirterek başlatır.

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
| hasHeaders | boolean |  |

### getCommentChar() {#getCommentChar}
```
public char getCommentChar()
```


CSV verilerinin satırlarını yorumlamak için kullanılan karakteri alır.

 **Remarks:** 

Varsayılan değer '\\#' (numara işareti) dir.

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

**Returns:**
char - CSV verisinin satırlarını yorumlamak için kullanılan karakter.
### getDelimiter() {#getDelimiter}
```
public char getDelimiter()
```


Sütun ayırıcı olarak kullanılacak karakteri alır.

 **Remarks:** 

Varsayılan değer ',' (virgül).

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

**Returns:**
char - Sütun ayırıcı olarak kullanılacak karakter.
### getQuoteChar() {#getQuoteChar}
```
public char getQuoteChar()
```


Alan değerlerini tırnak içine almak için kullanılan karakteri alır.

 **Remarks:** 

Varsayılan değer '"' (tırnak işareti).

Alıntı içinde yer alması için karakteri iki kez yazın.

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

**Returns:**
char - Alan değerlerini tırnak içine almak için kullanılan karakter.
### hasHeaders() {#hasHeaders}
```
public boolean hasHeaders()
```


CSV verilerinin ilk kaydının sütun adları içerip içermediğini gösteren bir değeri alır.

 **Remarks:** 

Varsayılan değer  false  dır.

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

**Returns:**
boolean - CSV verisinin ilk kaydının sütun adlarını içerip içermediğini belirten bir değer.
### hasHeaders(boolean value) {#hasHeaders-boolean}
```
public void hasHeaders(boolean value)
```


CSV verilerinin ilk kaydının sütun adları içerip içermediğini gösteren bir değeri ayarlar.

 **Remarks:** 

Varsayılan değer  false  dır.

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
| değer | boolean | CSV verisinin ilk kaydının sütun adlarını içerip içermediğini belirten bir değer. |

### setCommentChar(char value) {#setCommentChar-char}
```
public void setCommentChar(char value)
```


CSV verilerinin satırlarını yorumlamak için kullanılan karakteri ayarlar.

 **Remarks:** 

Varsayılan değer '\\#' (numara işareti) dir.

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
| değer | char | CSV verisinin satırlarını yorumlamak için kullanılan karakter. |

### setDelimiter(char value) {#setDelimiter-char}
```
public void setDelimiter(char value)
```


Sütun ayırıcı olarak kullanılacak karakteri ayarlar.

 **Remarks:** 

Varsayılan değer ',' (virgül).

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
| değer | char | Sütun ayırıcı olarak kullanılacak karakter. |

### setQuoteChar(char value) {#setQuoteChar-char}
```
public void setQuoteChar(char value)
```


Alan değerlerini tırnak içine almak için kullanılan karakteri ayarlar.

 **Remarks:** 

Varsayılan değer '"' (tırnak işareti).

Alıntı içinde yer alması için karakteri iki kez yazın.

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
| değer | char | Alan değerlerini tırnak içine almak için kullanılan karakter. |

