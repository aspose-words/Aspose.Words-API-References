---
title: "Comparer"
linktitle: "Comparer"
second_title: "Aspose.Words Java için"
description: "Java'da belgeleri karşılaştırmak için tasarlanmış yöntemler sağlar."
type: docs
weight: 114
url: /tr/java/com.aspose.words/comparer/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Comparer extends Processor
```

Belgeleri karşılaştırmak için tasarlanmış yöntemler sağlar.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date) |  |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) |  |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date) |  |
| [compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) |  |
| [compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime)](#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date) | İki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen çıktı dosyasına sağlanan kaydetme formatında kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir. |
| [compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | İki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen çıktı dosyasına sağlanan kaydetme formatında kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir. |
| [compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime)](#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date) |  |
| [compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) |  |
| [compare(String v1, String v2, String outputFileName, String author, Date dateTime)](#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date) | İki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen çıktı dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir. |
| [compare(String v1, String v2, String outputFileName, String author, Date dateTime, CompareOptions compareOptions)](#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | İki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen çıktı dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir. |
| [compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)](#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date) | İki belgeyi karşılaştırır ve farkları görüntü olarak kaydeder. |
| [compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | İki belgeyi karşılaştırır ve farkları görüntü olarak kaydeder. |
| [compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)](#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date) | İki belgeyi karşılaştırır ve farkları görüntü olarak kaydeder. |
| [compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)](#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions) | İki belgeyi karşılaştırır ve farkları görüntü olarak kaydeder. |
| [create()](#create) | Dönüştürücü işlemcisinin yeni bir örneğini oluşturur. |
| [create(ComparerContext context)](#create-com.aspose.words.ComparerContext) | Karşılaştırıcı işlemcisinin yeni bir örneğini oluşturur. |
| [execute()](#execute) | İşlemci eylemini çalıştır. |
| [from(InputStream input)](#from-java.io.InputStream) | İşleme için giriş belgesini belirtir. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | İşleme için giriş belgesini belirtir. |
| [from(String input)](#from-java.lang.String) | İşleme için giriş belgesini belirtir. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | İşleme için giriş belgesini belirtir. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | İşlemci için çıktı dosyasını belirtir. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | İşlemci için çıktı dosyasını belirtir. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| yazar | java.lang.String |  |
| dateTime | java.util.Date |  |

### compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| yazar | java.lang.String |  |
| dateTime | java.util.Date |  |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) |  |

### compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| yazar | java.lang.String |  |
| dateTime | java.util.Date |  |

### compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.io.InputStream-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(InputStream v1, InputStream v2, OutputStream outputStream, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | java.io.InputStream |  |
| v2 | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| yazar | java.lang.String |  |
| dateTime | java.util.Date |  |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) |  |

### compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime) {#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date}
```
public static void compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime)
```


İki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen çıktı dosyasına sağlanan kaydetme formatında kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | java.lang.String | Orijinal belge. |
| v2 | java.lang.String | Değiştirilmiş belge. |
| outputFileName | java.lang.String | Çıktı dosya adı. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Çıktının kaydetme seçenekleri. |
| yazar | java.lang.String | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | java.util.Date | Revizyonlar için kullanılacak tarih ve saat. |

### compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(String v1, String v2, String outputFileName, SaveOptions saveOptions, String author, Date dateTime, CompareOptions compareOptions)
```


İki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen çıktı dosyasına sağlanan kaydetme formatında kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | java.lang.String | Orijinal belge. |
| v2 | java.lang.String | Değiştirilmiş belge. |
| outputFileName | java.lang.String | Çıktı dosya adı. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Çıktının kaydetme seçenekleri. |
| yazar | java.lang.String | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | java.util.Date | Revizyonlar için kullanılacak tarih ve saat. |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | Belge karşılaştırma seçenekleri. |

### compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime) {#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date}
```
public static void compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | java.lang.String |  |
| v2 | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| yazar | java.lang.String |  |
| dateTime | java.util.Date |  |

### compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.lang.String-java.lang.String-java.lang.String-int-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(String v1, String v2, String outputFileName, int saveFormat, String author, Date dateTime, CompareOptions compareOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | java.lang.String |  |
| v2 | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| yazar | java.lang.String |  |
| dateTime | java.util.Date |  |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) |  |

### compare(String v1, String v2, String outputFileName, String author, Date dateTime) {#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date}
```
public static void compare(String v1, String v2, String outputFileName, String author, Date dateTime)
```


İki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen çıktı dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | java.lang.String | Orijinal belge. |
| v2 | java.lang.String | Değiştirilmiş belge. |
| outputFileName | java.lang.String | Çıktı dosya adı. |
| yazar | java.lang.String | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | java.util.Date | Revizyonlar için kullanılacak tarih ve saat. |

### compare(String v1, String v2, String outputFileName, String author, Date dateTime, CompareOptions compareOptions) {#compare-java.lang.String-java.lang.String-java.lang.String-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static void compare(String v1, String v2, String outputFileName, String author, Date dateTime, CompareOptions compareOptions)
```


İki belgeyi ek seçeneklerle karşılaştırır ve farkları belirtilen çıktı dosyasına kaydeder, değişiklikleri bir dizi düzenleme ve biçim revizyonu olarak üretir.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

 **Examples:** 

Belgeleri basitçe karşılaştırmanın nasıl yapılacağını gösterir.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.1.docx", "Author", new Date());
 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.2.docx", SaveFormat.DOCX, "Author", new Date());
 CompareOptions options = new CompareOptions();
 options.setIgnoreCaseChanges(true);
 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.3.docx", "Author", new Date(), options);
 Comparer.compare(firstDoc, secondDoc, getArtifactsDir() + "LowCode.CompareDocuments.4.docx", SaveFormat.DOCX, "Author", new Date(), options);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | java.lang.String | Orijinal belge. |
| v2 | java.lang.String | Değiştirilmiş belge. |
| outputFileName | java.lang.String | Çıktı dosya adı. |
| yazar | java.lang.String | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | java.util.Date | Revizyonlar için kullanılacak tarih ve saat. |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | Belge karşılaştırma seçenekleri. |

### compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime) {#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date}
```
public static OutputStream[] compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)
```


İki belgeyi karşılaştırır ve farkları görüntüler olarak kaydeder. Döndürülen dizideki her öğe, çıktının tek bir sayfasının görüntü olarak render edilmesini temsil eder.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | java.io.InputStream | Orijinal belge. |
| v2 | java.io.InputStream | Değiştirilmiş belge. |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Çıktının görüntü kaydetme seçenekleri. |
| yazar | java.lang.String | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | java.util.Date | Revizyonlar için kullanılacak tarih ve saat. |

**Returns:**
java.io.OutputStream[]
### compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compareToImages-java.io.InputStream-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static OutputStream[] compareToImages(InputStream v1, InputStream v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)
```


İki belgeyi karşılaştırır ve farkları görüntüler olarak kaydeder. Döndürülen dizideki her öğe, çıktının tek bir sayfasının görüntü olarak render edilmesini temsil eder.

 **Examples:** 

Belgeleri karşılaştırmayı ve sonuçları görüntüler olarak kaydetmeyi gösterir.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 OutputStream[] pages = Comparer.compareToImages(firstDoc, secondDoc, new ImageSaveOptions(SaveFormat.PNG), "Author", new Date());

 try (FileInputStream firstStreamIn = new FileInputStream(firstDoc)) {
     try (FileInputStream secondStreamIn = new FileInputStream(secondDoc)) {
         CompareOptions compareOptions = new CompareOptions();
         compareOptions.setIgnoreCaseChanges(true);
         pages = Comparer.compareToImages(firstStreamIn, secondStreamIn, new ImageSaveOptions(SaveFormat.PNG), "Author", new Date(), compareOptions);
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | java.io.InputStream | Orijinal belge. |
| v2 | java.io.InputStream | Değiştirilmiş belge. |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Çıktının görüntü kaydetme seçenekleri. |
| yazar | java.lang.String | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | java.util.Date | Revizyonlar için kullanılacak tarih ve saat. |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | Belge karşılaştırma seçenekleri. |

**Returns:**
java.io.OutputStream[]
### compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime) {#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date}
```
public static OutputStream[] compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime)
```


İki belgeyi karşılaştırır ve farkları görüntüler olarak kaydeder. Döndürülen dizideki her öğe, çıktının tek bir sayfasının görüntü olarak render edilmesini temsil eder.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | java.lang.String | Orijinal belge. |
| v2 | java.lang.String | Değiştirilmiş belge. |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Çıktının görüntü kaydetme seçenekleri. |
| yazar | java.lang.String | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | java.util.Date | Revizyonlar için kullanılacak tarih ve saat. |

**Returns:**
java.io.OutputStream[]
### compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions) {#compareToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.util.Date-com.aspose.words.CompareOptions}
```
public static OutputStream[] compareToImages(String v1, String v2, ImageSaveOptions imageSaveOptions, String author, Date dateTime, CompareOptions compareOptions)
```


İki belgeyi karşılaştırır ve farkları görüntüler olarak kaydeder. Döndürülen dizideki her öğe, çıktının tek bir sayfasının görüntü olarak render edilmesini temsil eder.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| v1 | java.lang.String | Orijinal belge. |
| v2 | java.lang.String | Değiştirilmiş belge. |
| imageSaveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Çıktının görüntü kaydetme seçenekleri. |
| yazar | java.lang.String | Revizyonlar için kullanılacak yazarın baş harfleri. |
| dateTime | java.util.Date | Revizyonlar için kullanılacak tarih ve saat. |
| compareOptions | [CompareOptions](../../com.aspose.words/compareoptions/) | Belge karşılaştırma seçenekleri. |

**Returns:**
java.io.OutputStream[]
### create() {#create}
```
public static Comparer create()
```


Dönüştürücü işlemcisinin yeni bir örneğini oluşturur.

**Returns:**
[Comparer](../../com.aspose.words/comparer/)
### create(ComparerContext context) {#create-com.aspose.words.ComparerContext}
```
public static Comparer create(ComparerContext context)
```


Karşılaştırıcı işlemcisinin yeni bir örneğini oluşturur.

 **Examples:** 

Bağlam kullanarak belgeleri basitçe karşılaştırmanın nasıl yapılacağını gösterir.

```

 // There is a several ways to compare documents:
 String firstDoc = getMyDir() + "Table column bookmarks.docx";
 String secondDoc = getMyDir() + "Table column bookmarks.doc";

 ComparerContext comparerContext = new ComparerContext();
 comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
 comparerContext.setAuthor("Author");
 comparerContext.setDateTime(new Date());

 Comparer.create(comparerContext)
         .from(firstDoc)
         .from(secondDoc)
         .to(getArtifactsDir() + "LowCode.CompareContextDocuments.docx")
         .execute();
 
```

Bağlam kullanarak akıştan belgeleri karşılaştırmanın nasıl yapılacağını gösterir.

```

 // There is a several ways to compare documents from the stream:
 try (FileInputStream firstStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.docx")) {
     try (FileInputStream secondStreamIn = new FileInputStream(getMyDir() + "Table column bookmarks.doc")) {
         ComparerContext comparerContext = new ComparerContext();
         comparerContext.getCompareOptions().setIgnoreCaseChanges(true);
         comparerContext.setAuthor("Author");
         comparerContext.setDateTime(new Date());

         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.CompareContextStreamDocuments.docx")) {
             Comparer.create(comparerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| context | [ComparerContext](../../com.aspose.words/comparercontext/) |  |

**Returns:**
[Comparer](../../com.aspose.words/comparer/)
### execute() {#execute}
```
public void execute()
```


İşlemci eylemini çalıştır.

 **Examples:** 

Bağlamı kullanarak belgeleri tek bir çıktı belgesine birleştirmenin nasıl yapılacağını gösterir.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

Bağlamı kullanarak akıştan belgeleri tek bir çıktı belgesine birleştirmenin nasıl yapılacağını gösterir.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 try (FileInputStream firstStreamIn = new FileInputStream(inputDoc1)) {
     try (FileInputStream secondStreamIn = new FileInputStream(inputDoc2)) {
         OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
         {
             saveOptions.setPassword("Aspose.Words");
         }
         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.1.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, saveOptions)
                     .execute();
         }

         LoadOptions firstLoadOptions = new LoadOptions();
         {
             firstLoadOptions.setIgnoreOleData(true);
         }
         LoadOptions secondLoadOptions = new LoadOptions();
         {
             secondLoadOptions.setIgnoreOleData(false);
         }
         try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.2.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn, firstLoadOptions)
                     .from(secondStreamIn, secondLoadOptions)
                     .to(streamOut1, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

Bağlamı kullanarak tek bir kod satırıyla belgeleri dönüştürmenin nasıl yapılacağını gösterir.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

Bağlamı kullanarak akıştan belgeleri tek bir kod satırıyla dönüştürmenin nasıl yapılacağını gösterir.

```

 String doc = getMyDir() + "Document.docx";
 ConverterContext converterContext = new ConverterContext();

 try (FileInputStream streamIn = new FileInputStream(doc)) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.1.docx")) {
         Converter.create(converterContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.RTF)
                 .execute();
     }

     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
     {
         saveOptions.setPassword("Aspose.Words");
     }
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(true);
     }
     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.2.docx")) {
         Converter.create(converterContext)
                 .from(streamIn, loadOptions)
                 .to(streamOut1, saveOptions)
                 .execute();
     }
 }
 
```

### from(InputStream input) {#from-java.io.InputStream}
```
public Processor from(InputStream input)
```


İşleme için giriş belgesini belirtir.

 **Remarks:** 

İşlemci yalnızca bir dosyayı girdi olarak kabul ediyorsa, yalnızca son belirtilen dosya işlenecektir. [Merger](../../com.aspose.words/merger/) işlemcisi birden fazla dosyayı girdi olarak kabul eder, bu nedenle belirtilen tüm belgeler birleştirilecektir. [Converter](../../com.aspose.words/converter/) işlemcisi yalnızca bir dosyayı girdi olarak kabul eder, bu yüzden yalnızca son belirtilen dosya dönüştürülecektir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| girdi | java.io.InputStream | Girdi belge akışı. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


İşleme için giriş belgesini belirtir.

 **Remarks:** 

İşlemci yalnızca bir dosyayı girdi olarak kabul ediyorsa, yalnızca son belirtilen dosya işlenecektir. [Merger](../../com.aspose.words/merger/) işlemcisi birden fazla dosyayı girdi olarak kabul eder, bu nedenle belirtilen tüm belgeler birleştirilecektir. [Converter](../../com.aspose.words/converter/) işlemcisi yalnızca bir dosyayı girdi olarak kabul eder, bu yüzden yalnızca son belirtilen dosya dönüştürülecektir.

 **Examples:** 

Bağlamı kullanarak akıştan belgeleri tek bir çıktı belgesine birleştirmenin nasıl yapılacağını gösterir.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 try (FileInputStream firstStreamIn = new FileInputStream(inputDoc1)) {
     try (FileInputStream secondStreamIn = new FileInputStream(inputDoc2)) {
         OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
         {
             saveOptions.setPassword("Aspose.Words");
         }
         try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.1.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn)
                     .from(secondStreamIn)
                     .to(streamOut, saveOptions)
                     .execute();
         }

         LoadOptions firstLoadOptions = new LoadOptions();
         {
             firstLoadOptions.setIgnoreOleData(true);
         }
         LoadOptions secondLoadOptions = new LoadOptions();
         {
             secondLoadOptions.setIgnoreOleData(false);
         }
         try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.MergeStreamContextDocuments.2.docx")) {
             Merger.create(mergerContext)
                     .from(firstStreamIn, firstLoadOptions)
                     .from(secondStreamIn, secondLoadOptions)
                     .to(streamOut1, SaveFormat.DOCX)
                     .execute();
         }
     }
 }
 
```

Bağlamı kullanarak akıştan belgeleri tek bir kod satırıyla dönüştürmenin nasıl yapılacağını gösterir.

```

 String doc = getMyDir() + "Document.docx";
 ConverterContext converterContext = new ConverterContext();

 try (FileInputStream streamIn = new FileInputStream(doc)) {
     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.1.docx")) {
         Converter.create(converterContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.RTF)
                 .execute();
     }

     OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
     {
         saveOptions.setPassword("Aspose.Words");
     }
     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(true);
     }
     try (FileOutputStream streamOut1 = new FileOutputStream(getArtifactsDir() + "LowCode.ConvertContextStream.2.docx")) {
         Converter.create(converterContext)
                 .from(streamIn, loadOptions)
                 .to(streamOut1, saveOptions)
                 .execute();
     }
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| girdi | java.io.InputStream | Girdi belge akışı. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Belgeyi yüklemek için kullanılan isteğe bağlı yükleme seçenekleri. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


İşleme için giriş belgesini belirtir.

 **Remarks:** 

İşlemci yalnızca bir dosyayı girdi olarak kabul ediyorsa, yalnızca son belirtilen dosya işlenecektir. [Merger](../../com.aspose.words/merger/) işlemcisi birden fazla dosyayı girdi olarak kabul eder, bu nedenle belirtilen tüm belgeler birleştirilecektir. [Converter](../../com.aspose.words/converter/) işlemcisi yalnızca bir dosyayı girdi olarak kabul eder, bu yüzden yalnızca son belirtilen dosya dönüştürülecektir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| girdi | java.lang.String | Girdi belge dosya adı. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


İşleme için giriş belgesini belirtir.

 **Remarks:** 

İşlemci yalnızca bir dosyayı girdi olarak kabul ediyorsa, yalnızca son belirtilen dosya işlenecektir. [Merger](../../com.aspose.words/merger/) işlemcisi birden fazla dosyayı girdi olarak kabul eder, bu nedenle belirtilen tüm belgeler birleştirilecektir. [Converter](../../com.aspose.words/converter/) işlemcisi yalnızca bir dosyayı girdi olarak kabul eder, bu yüzden yalnızca son belirtilen dosya dönüştürülecektir.

 **Examples:** 

Bağlamı kullanarak belgeleri tek bir çıktı belgesine birleştirmenin nasıl yapılacağını gösterir.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

Bağlamı kullanarak tek bir kod satırıyla belgeleri dönüştürmenin nasıl yapılacağını gösterir.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| girdi | java.lang.String | Girdi belge dosya adı. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Belgeyi yüklemek için kullanılan isteğe bağlı yükleme seçenekleri. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


İşlemci için çıktı dosyasını belirtir.

 **Remarks:** 

Çıktı birden fazla dosyadan oluşuyorsa, belirtilen çıktı dosya adı, her bölüm için 'outputFile\_partIndex.extension' kuralına göre dosya adı oluşturmak için kullanılır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.lang.String | Çıktı dosya adı. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


İşlemci için çıktı dosyasını belirtir.

 **Remarks:** 

Çıktı birden fazla dosyadan oluşuyorsa, belirtilen çıktı dosya adı, her bölüm için 'outputFile\_partIndex.extension' kuralına göre dosya adı oluşturmak için kullanılır.

 **Examples:** 

Bağlamı kullanarak belgeleri tek bir çıktı belgesine birleştirmenin nasıl yapılacağını gösterir.

```

 //There is a several ways to merge documents:
 String inputDoc1 = getMyDir() + "Big document.docx";
 String inputDoc2 = getMyDir() + "Tables.docx";

 MergerContext mergerContext = new MergerContext();
 mergerContext.setMergeFormatMode(MergeFormatMode.KEEP_SOURCE_FORMATTING);

 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.1.docx")
         .execute();

 LoadOptions firstLoadOptions = new LoadOptions();
 {
     firstLoadOptions.setIgnoreOleData(true);
 }
 LoadOptions secondLoadOptions = new LoadOptions();
 {
     secondLoadOptions.setIgnoreOleData(false);
 }
 Merger.create(mergerContext)
         .from(inputDoc1, firstLoadOptions)
         .from(inputDoc2, secondLoadOptions)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.2.docx", SaveFormat.DOCX)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 Merger.create(mergerContext)
         .from(inputDoc1)
         .from(inputDoc2)
         .to(getArtifactsDir() + "LowCode.MergeContextDocuments.3.docx", saveOptions)
         .execute();
 
```

Bağlamı kullanarak tek bir kod satırıyla belgeleri dönüştürmenin nasıl yapılacağını gösterir.

```

 String doc = getMyDir() + "Big document.docx";

 ConverterContext converterContext = new ConverterContext();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.1.pdf")
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.2.pdf", SaveFormat.RTF)
         .execute();

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.create(converterContext)
         .from(doc, loadOptions)
         .to(getArtifactsDir() + "LowCode.ConvertContext.3.docx", saveOptions)
         .execute();

 Converter.create(converterContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ConvertContext.4.png", new ImageSaveOptions(SaveFormat.PNG))
         .execute();
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.lang.String | Çıktı dosya adı. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | İsteğe bağlı kaydetme seçenekleri. Belirtilmezse, kaydetme biçimi dosya uzantısına göre belirlenir. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| çıktı | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
