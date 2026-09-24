---
title: "Converter"
linktitle: "Converter"
second_title: "Aspose.Words Java için"
description: "Java'da tek bir kod satırıyla çeşitli belge türlerini dönüştürmek için tasarlanmış bir grup yöntemi temsil eder."
type: docs
weight: 132
url: /tr/java/com.aspose.words/converter/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Converter extends Processor
```

Tek bir kod satırıyla çeşitli belge türlerini dönüştürmek için tasarlanmış bir yöntem grubunu temsil eder.

 **Remarks:** 

Belirtilen giriş ve çıkış dosyaları veya akışları, istenen kaydetme formatı ile birlikte, verilen giriş belgesini bir formattan diğer belirtilen formata dönüştürmek için kullanılır.

Dönüştürme işlevi 35'ten fazla farklı dosya formatını destekler.

The **M:Aspose.Words.LowCode.Converter.ConvertToImages(System.String,Aspose.Words.SaveFormat)** yöntem grubu, belgeleri görüntülere dönüştürmek için tasarlanmıştır; her sayfa ayrı bir görüntü dosyasına dönüştürülür. Bu yöntemler ayrıca PDF belgelerini belge modeline yüklemeden doğrudan sabit sayfa formatlarına dönüştürür, bu da performans ve doğruluğu artırır.

Bu yöntemle [ImageSaveOptions.getPageSet()](../../com.aspose.words/imagesaveoptions/\#getPageSet) / [ImageSaveOptions.setPageSet(com.aspose.words.PageSet)](../../com.aspose.words/imagesaveoptions/\#setPageSet-com.aspose.words.PageSet) kullanarak, görüntülere dönüştürülecek belirli bir sayfa kümesini belirtebilirsiniz.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convert(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convert(InputStream inputStream, OutputStream outputStream, int saveFormat)](#convert-java.io.InputStream-java.io.OutputStream-int) |  |
| [convert(String inputFile, LoadOptions loadOptions, String outputFile, SaveOptions saveOptions)](#convert-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.SaveOptions) | Belirtilen giriş ve çıkış dosya adları ve yükleme/kaydetme seçeneklerini kullanarak verilen giriş belgesini çıkış belgesine dönüştürür. |
| [convert(String inputFile, String outputFile)](#convert-java.lang.String-java.lang.String) | Belirtilen giriş ve çıkış dosya adları ve uzantılarını kullanarak verilen giriş belgesini çıktı belgesine dönüştürür. |
| [convert(String inputFile, String outputFile, SaveOptions saveOptions)](#convert-java.lang.String-java.lang.String-com.aspose.words.SaveOptions) | Belirtilen giriş ve çıkış dosya adları ve kaydetme seçeneklerini kullanarak verilen giriş belgesini çıktı belgesine dönüştürür. |
| [convert(String inputFile, String outputFile, int saveFormat)](#convert-java.lang.String-java.lang.String-int) |  |
| [convertToImages(Document doc, ImageSaveOptions saveOptions)](#convertToImages-com.aspose.words.Document-com.aspose.words.ImageSaveOptions) | Belirtilen belgenin sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür. |
| [convertToImages(Document doc, int saveFormat)](#convertToImages-com.aspose.words.Document-int) |  |
| [convertToImages(InputStream inputStream, ImageSaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions) | Belirtilen giriş akışının sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür. |
| [convertToImages(InputStream inputStream, LoadOptions loadOptions, ImageSaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.ImageSaveOptions) | Belirtilen giriş akışının sayfalarını sağlanan yükleme ve kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür. |
| [convertToImages(InputStream inputStream, int saveFormat)](#convertToImages-java.io.InputStream-int) |  |
| [convertToImages(String inputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-com.aspose.words.ImageSaveOptions) | Belirtilen giriş dosyasının sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür. |
| [convertToImages(String inputFile, LoadOptions loadOptions, String outputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.ImageSaveOptions) | Belirtilen giriş dosyasının sayfalarını sağlanan yükleme ve kaydetme seçeneklerini kullanarak görüntü dosyalarına dönüştürür. |
| [convertToImages(String inputFile, int saveFormat)](#convertToImages-java.lang.String-int) |  |
| [convertToImages(String inputFile, String outputFile)](#convertToImages-java.lang.String-java.lang.String) | Belirtilen giriş dosyasının sayfalarını görüntü dosyalarına dönüştürür. |
| [convertToImages(String inputFile, String outputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions) | Belirtilen giriş dosyasının sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntü dosyalarına dönüştürür. |
| [convertToImages(String inputFile, String outputFile, int saveFormat)](#convertToImages-java.lang.String-java.lang.String-int) |  |
| [create()](#create) | Dönüştürücü işlemcisinin yeni bir örneğini oluşturur. |
| [create(ConverterContext context)](#create-com.aspose.words.ConverterContext) | Dönüştürücü işlemcisinin yeni bir örneğini oluşturur. |
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
### convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions) {#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public static void convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### convert(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions) {#convert-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public static void convert(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### convert(InputStream inputStream, OutputStream outputStream, int saveFormat) {#convert-java.io.InputStream-java.io.OutputStream-int}
```
public static void convert(InputStream inputStream, OutputStream outputStream, int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |

### convert(String inputFile, LoadOptions loadOptions, String outputFile, SaveOptions saveOptions) {#convert-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.SaveOptions}
```
public static void convert(String inputFile, LoadOptions loadOptions, String outputFile, SaveOptions saveOptions)
```


Belirtilen giriş ve çıkış dosya adları ve yükleme/kaydetme seçeneklerini kullanarak verilen giriş belgesini çıkış belgesine dönüştürür.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

 **Examples:** 

Belgeleri tek bir kod satırıyla nasıl dönüştüreceğinizi gösterir.

```

 String doc = getMyDir() + "Document.docx";

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.pdf");

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveFormat.rtf", SaveFormat.RTF);

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.convert(doc, loadOptions, getArtifactsDir() + "LowCode.Convert.LoadOptions.docx", saveOptions);

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveOptions.docx", saveOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | java.lang.String | Girdi dosya adı. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Giriş belgesi yükleme seçenekleri. |
| outputFile | java.lang.String | Çıktı dosya adı. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Kaydetme seçenekleri. |

### convert(String inputFile, String outputFile) {#convert-java.lang.String-java.lang.String}
```
public static void convert(String inputFile, String outputFile)
```


Belirtilen giriş ve çıkış dosya adları ve uzantılarını kullanarak verilen giriş belgesini çıktı belgesine dönüştürür.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

 **Examples:** 

Belgeleri tek bir kod satırıyla nasıl dönüştüreceğinizi gösterir.

```

 String doc = getMyDir() + "Document.docx";

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.pdf");

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveFormat.rtf", SaveFormat.RTF);

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.convert(doc, loadOptions, getArtifactsDir() + "LowCode.Convert.LoadOptions.docx", saveOptions);

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveOptions.docx", saveOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | java.lang.String | Girdi dosya adı. |
| outputFile | java.lang.String | Çıktı dosya adı. |

### convert(String inputFile, String outputFile, SaveOptions saveOptions) {#convert-java.lang.String-java.lang.String-com.aspose.words.SaveOptions}
```
public static void convert(String inputFile, String outputFile, SaveOptions saveOptions)
```


Belirtilen giriş ve çıkış dosya adları ve kaydetme seçeneklerini kullanarak verilen giriş belgesini çıktı belgesine dönüştürür.

 **Remarks:** 

Çıktı formatı bir görüntü (BMP, EMF, EPS, GIF, JPEG, PNG veya WebP) ise, çıktının her sayfası ayrı bir dosya olarak kaydedilir. Belirtilen çıktı dosya adı, her bölüm için dosya adlarını şu kurala göre oluşturmak için kullanılır: outputFile\_partIndex.extension.

Çıktı formatı TIFF ise, çıktı tek bir çok çerçeveli TIFF dosyası olarak kaydedilir.

 **Examples:** 

Belgeleri tek bir kod satırıyla nasıl dönüştüreceğinizi gösterir.

```

 String doc = getMyDir() + "Document.docx";

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.pdf");

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveFormat.rtf", SaveFormat.RTF);

 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
 {
     saveOptions.setPassword("Aspose.Words");
 }
 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(true);
 }
 Converter.convert(doc, loadOptions, getArtifactsDir() + "LowCode.Convert.LoadOptions.docx", saveOptions);

 Converter.convert(doc, getArtifactsDir() + "LowCode.Convert.SaveOptions.docx", saveOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | java.lang.String | Girdi dosya adı. |
| outputFile | java.lang.String | Çıktı dosya adı. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Kaydetme seçenekleri. |

### convert(String inputFile, String outputFile, int saveFormat) {#convert-java.lang.String-java.lang.String-int}
```
public static void convert(String inputFile, String outputFile, int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | java.lang.String |  |
| outputFile | java.lang.String |  |
| saveFormat | int |  |

### convertToImages(Document doc, ImageSaveOptions saveOptions) {#convertToImages-com.aspose.words.Document-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(Document doc, ImageSaveOptions saveOptions)
```


Belirtilen belgenin sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür.

 **Examples:** 

Belgeyi görüntü akışına nasıl dönüştüreceğinizi gösterir.

```

 String doc = getMyDir() + "Big document.docx";

 OutputStream[] streams = Converter.convertToImages(doc, SaveFormat.PNG);

 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 streams = Converter.convertToImages(doc, imageSaveOptions);

 streams = Converter.convertToImages(new Document(doc), SaveFormat.PNG);

 streams = Converter.convertToImages(new Document(doc), imageSaveOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | Giriş belgesi. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Görüntü kaydetme seçenekleri. |

**Returns:**
java.io.OutputStream[] - Görüntü akışlarının bir dizisini döndürür. Akışlar son kullanıcı tarafından serbest bırakılmalıdır.
### convertToImages(Document doc, int saveFormat) {#convertToImages-com.aspose.words.Document-int}
```
public static OutputStream[] convertToImages(Document doc, int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| saveFormat | int |  |

**Returns:**
java.io.OutputStream[]
### convertToImages(InputStream inputStream, ImageSaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(InputStream inputStream, ImageSaveOptions saveOptions)
```


Belirtilen giriş akışının sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür.

 **Examples:** 

Belgeyi akıştan görüntülere nasıl dönüştüreceğinizi gösterir.

```

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Big document.docx")) {
     OutputStream[] streams = Converter.convertToImages(streamIn, SaveFormat.JPEG);

     ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
     imageSaveOptions.setPageSet(new PageSet(1));
     streams = Converter.convertToImages(streamIn, imageSaveOptions);

     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(false);
     }
     Converter.convertToImages(streamIn, loadOptions, imageSaveOptions);
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | java.io.InputStream | Girdi akışı. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Görüntü kaydetme seçenekleri. |

**Returns:**
java.io.OutputStream[] - Görüntü akışlarının bir dizisini döndürür. Akışlar son kullanıcı tarafından serbest bırakılmalıdır.
### convertToImages(InputStream inputStream, LoadOptions loadOptions, ImageSaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(InputStream inputStream, LoadOptions loadOptions, ImageSaveOptions saveOptions)
```


Belirtilen giriş akışının sayfalarını sağlanan yükleme ve kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür.

 **Examples:** 

Belgeyi akıştan görüntülere nasıl dönüştüreceğinizi gösterir.

```

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Big document.docx")) {
     OutputStream[] streams = Converter.convertToImages(streamIn, SaveFormat.JPEG);

     ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
     imageSaveOptions.setPageSet(new PageSet(1));
     streams = Converter.convertToImages(streamIn, imageSaveOptions);

     LoadOptions loadOptions = new LoadOptions();
     {
         loadOptions.setIgnoreOleData(false);
     }
     Converter.convertToImages(streamIn, loadOptions, imageSaveOptions);
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | java.io.InputStream | Girdi akışı. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Giriş belgesi yükleme seçenekleri. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Görüntü kaydetme seçenekleri. |

**Returns:**
java.io.OutputStream[] - Görüntü akışlarının bir dizisini döndürür. Akışlar son kullanıcı tarafından serbest bırakılmalıdır.
### convertToImages(InputStream inputStream, int saveFormat) {#convertToImages-java.io.InputStream-int}
```
public static OutputStream[] convertToImages(InputStream inputStream, int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| saveFormat | int |  |

**Returns:**
java.io.OutputStream[]
### convertToImages(String inputFile, ImageSaveOptions saveOptions) {#convertToImages-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(String inputFile, ImageSaveOptions saveOptions)
```


Belirtilen giriş dosyasının sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntülere dönüştürür ve görüntüleri içeren akışların bir dizisini döndürür.

 **Examples:** 

Belgeyi görüntü akışına nasıl dönüştüreceğinizi gösterir.

```

 String doc = getMyDir() + "Big document.docx";

 OutputStream[] streams = Converter.convertToImages(doc, SaveFormat.PNG);

 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 streams = Converter.convertToImages(doc, imageSaveOptions);

 streams = Converter.convertToImages(new Document(doc), SaveFormat.PNG);

 streams = Converter.convertToImages(new Document(doc), imageSaveOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | java.lang.String | Girdi dosya adı. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Görüntü kaydetme seçenekleri. |

**Returns:**
java.io.OutputStream[] - Görüntü akışlarının bir dizisini döndürür. Akışlar son kullanıcı tarafından serbest bırakılmalıdır.
### convertToImages(String inputFile, LoadOptions loadOptions, String outputFile, ImageSaveOptions saveOptions) {#convertToImages-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public static void convertToImages(String inputFile, LoadOptions loadOptions, String outputFile, ImageSaveOptions saveOptions)
```


Belirtilen giriş dosyasının sayfalarını sağlanan yükleme ve kaydetme seçeneklerini kullanarak görüntü dosyalarına dönüştürür.

 **Examples:** 

Belgeyi görüntülere nasıl dönüştüreceğinizi gösterir.

```

 String doc = getMyDir() + "Big document.docx";

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.1.png");

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.2.jpeg", SaveFormat.JPEG);

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(false);
 }
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 Converter.convertToImages(doc, loadOptions, getArtifactsDir() + "LowCode.ConvertToImages.3.png", imageSaveOptions);

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.4.png", imageSaveOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | java.lang.String | Girdi dosya adı. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Giriş belgesi yükleme seçenekleri. |
| outputFile | java.lang.String | Sayfa görüntüleri için dosya adını "outputFile\\_pageIndex.extension" kuralını kullanarak oluşturmak için kullanılan çıktı dosya adı. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Görüntü kaydetme seçenekleri. |

### convertToImages(String inputFile, int saveFormat) {#convertToImages-java.lang.String-int}
```
public static OutputStream[] convertToImages(String inputFile, int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
java.io.OutputStream[]
### convertToImages(String inputFile, String outputFile) {#convertToImages-java.lang.String-java.lang.String}
```
public static void convertToImages(String inputFile, String outputFile)
```


Belirtilen giriş dosyasının sayfalarını görüntü dosyalarına dönüştürür.

 **Examples:** 

Belgeyi görüntülere nasıl dönüştüreceğinizi gösterir.

```

 String doc = getMyDir() + "Big document.docx";

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.1.png");

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.2.jpeg", SaveFormat.JPEG);

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(false);
 }
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 Converter.convertToImages(doc, loadOptions, getArtifactsDir() + "LowCode.ConvertToImages.3.png", imageSaveOptions);

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.4.png", imageSaveOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | java.lang.String | Girdi dosya adı. |
| outputFile | java.lang.String | Sayfa görüntüleri için dosya adını "outputFile\\_pageIndex.extension" kuralını kullanarak oluşturmak için kullanılan çıktı dosya adı. |

### convertToImages(String inputFile, String outputFile, ImageSaveOptions saveOptions) {#convertToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public static void convertToImages(String inputFile, String outputFile, ImageSaveOptions saveOptions)
```


Belirtilen giriş dosyasının sayfalarını belirtilen kaydetme seçeneklerini kullanarak görüntü dosyalarına dönüştürür.

 **Examples:** 

Belgeyi görüntülere nasıl dönüştüreceğinizi gösterir.

```

 String doc = getMyDir() + "Big document.docx";

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.1.png");

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.2.jpeg", SaveFormat.JPEG);

 LoadOptions loadOptions = new LoadOptions();
 {
     loadOptions.setIgnoreOleData(false);
 }
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPageSet(new PageSet(1));
 Converter.convertToImages(doc, loadOptions, getArtifactsDir() + "LowCode.ConvertToImages.3.png", imageSaveOptions);

 Converter.convertToImages(doc, getArtifactsDir() + "LowCode.ConvertToImages.4.png", imageSaveOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | java.lang.String | Girdi dosya adı. |
| outputFile | java.lang.String | Sayfa görüntüleri için dosya adını "outputFile\\_pageIndex.extension" kuralını kullanarak oluşturmak için kullanılan çıktı dosya adı. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Görüntü kaydetme seçenekleri. |

### convertToImages(String inputFile, String outputFile, int saveFormat) {#convertToImages-java.lang.String-java.lang.String-int}
```
public static void convertToImages(String inputFile, String outputFile, int saveFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFile | java.lang.String |  |
| outputFile | java.lang.String |  |
| saveFormat | int |  |

### create() {#create}
```
public static Converter create()
```


Dönüştürücü işlemcisinin yeni bir örneğini oluşturur.

**Returns:**
[Converter](../../com.aspose.words/converter/)
### create(ConverterContext context) {#create-com.aspose.words.ConverterContext}
```
public static Converter create(ConverterContext context)
```


Dönüştürücü işlemcisinin yeni bir örneğini oluşturur.

 **Examples:** 

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| context | [ConverterContext](../../com.aspose.words/convertercontext/) |  |

**Returns:**
[Converter](../../com.aspose.words/converter/)
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
