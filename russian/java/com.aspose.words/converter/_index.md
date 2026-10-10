---
title: "Converter"
linktitle: "Converter"
second_title: "Aspose.Words для Java"
description: "Представляет группу методов, предназначенных для конвертации различных типов документов с помощью одной строки кода на Java."
type: docs
weight: 132
url: /ru/java/com.aspose.words/converter/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Converter extends Processor
```

Представляет группу методов, предназначенных для конвертации различных типов документов с помощью одной строки кода.

 **Remarks:** 

Указанные входные и выходные файлы или потоки, вместе с желаемым форматом сохранения, используются для преобразования входного документа из одного формата в выходной документ в другом указанном формате.

Функциональность конвертации поддерживает более 35 различных форматов файлов.

Группа методов **M:Aspose.Words.LowCode.Converter.ConvertToImages(System.String,Aspose.Words.SaveFormat)** предназначена для преобразования документов в изображения, при этом каждая страница конвертируется в отдельный файл изображения. Эти методы также преобразуют PDF‑документы напрямую в форматы фиксированных страниц без загрузки их в модель документа, что повышает как производительность, так и точность.

С помощью [ImageSaveOptions.getPageSet()](../../com.aspose.words/imagesaveoptions/\#getPageSet) / [ImageSaveOptions.setPageSet(com.aspose.words.PageSet)](../../com.aspose.words/imagesaveoptions/\#setPageSet-com.aspose.words.PageSet) можно указать конкретный набор страниц для преобразования в изображения.
## Методы

| Метод | Описание |
| --- | --- |
| [convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convert(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convert(InputStream inputStream, OutputStream outputStream, int saveFormat)](#convert-java.io.InputStream-java.io.OutputStream-int) |  |
| [convert(String inputFile, LoadOptions loadOptions, String outputFile, SaveOptions saveOptions)](#convert-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.SaveOptions) | Преобразует указанный входной документ в выходной документ, используя заданные имена файлов ввода‑вывода и их параметры загрузки/сохранения. |
| [convert(String inputFile, String outputFile)](#convert-java.lang.String-java.lang.String) | Преобразует заданный входной документ в выходной документ, используя указанные имена входного и выходного файлов и их расширения. |
| [convert(String inputFile, String outputFile, SaveOptions saveOptions)](#convert-java.lang.String-java.lang.String-com.aspose.words.SaveOptions) | Преобразует заданный входной документ в выходной документ, используя указанные имена входного и выходного файлов и параметры сохранения. |
| [convert(String inputFile, String outputFile, int saveFormat)](#convert-java.lang.String-java.lang.String-int) |  |
| [convertToImages(Document doc, ImageSaveOptions saveOptions)](#convertToImages-com.aspose.words.Document-com.aspose.words.ImageSaveOptions) | Преобразует страницы указанного документа в изображения, используя указанные параметры сохранения, и возвращает массив потоков, содержащих изображения. |
| [convertToImages(Document doc, int saveFormat)](#convertToImages-com.aspose.words.Document-int) |  |
| [convertToImages(InputStream inputStream, ImageSaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions) | Преобразует страницы указанного входного потока в изображения, используя указанные параметры сохранения, и возвращает массив потоков, содержащих изображения. |
| [convertToImages(InputStream inputStream, LoadOptions loadOptions, ImageSaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.ImageSaveOptions) | Преобразует страницы указанного входного потока в изображения, используя предоставленные параметры загрузки и сохранения, и возвращает массив потоков, содержащих изображения. |
| [convertToImages(InputStream inputStream, int saveFormat)](#convertToImages-java.io.InputStream-int) |  |
| [convertToImages(String inputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-com.aspose.words.ImageSaveOptions) | Преобразует страницы указанного входного файла в изображения, используя указанные параметры сохранения, и возвращает массив потоков, содержащих изображения. |
| [convertToImages(String inputFile, LoadOptions loadOptions, String outputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.ImageSaveOptions) | Преобразует страницы указанного входного файла в файлы изображений, используя предоставленные параметры загрузки и сохранения. |
| [convertToImages(String inputFile, int saveFormat)](#convertToImages-java.lang.String-int) |  |
| [convertToImages(String inputFile, String outputFile)](#convertToImages-java.lang.String-java.lang.String) | Преобразует страницы указанного входного файла в файлы изображений. |
| [convertToImages(String inputFile, String outputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions) | Преобразует страницы указанного входного файла в файлы изображений, используя указанные параметры сохранения. |
| [convertToImages(String inputFile, String outputFile, int saveFormat)](#convertToImages-java.lang.String-java.lang.String-int) |  |
| [create()](#create) | Создаёт новый экземпляр процессора конвертера. |
| [create(ConverterContext context)](#create-com.aspose.words.ConverterContext) | Создаёт новый экземпляр процессора конвертера. |
| [execute()](#execute) | Выполнить действие процессора. |
| [from(InputStream input)](#from-java.io.InputStream) | Указывает входной документ для обработки. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Указывает входной документ для обработки. |
| [from(String input)](#from-java.lang.String) | Указывает входной документ для обработки. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Указывает входной документ для обработки. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Указывает выходной файл для процессора. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Указывает выходной файл для процессора. |
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
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### convert(InputStream inputStream, OutputStream outputStream, int saveFormat) {#convert-java.io.InputStream-java.io.OutputStream-int}
```
public static void convert(InputStream inputStream, OutputStream outputStream, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |

### convert(String inputFile, LoadOptions loadOptions, String outputFile, SaveOptions saveOptions) {#convert-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.SaveOptions}
```
public static void convert(String inputFile, LoadOptions loadOptions, String outputFile, SaveOptions saveOptions)
```


Преобразует указанный входной документ в выходной документ, используя заданные имена файлов ввода‑вывода и их параметры загрузки/сохранения.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

 **Examples:** 

Показывает, как преобразовать документы одной строкой кода.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | java.lang.String | Имя входного файла. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Параметры загрузки входного документа. |
| outputFile | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Параметры сохранения. |

### convert(String inputFile, String outputFile) {#convert-java.lang.String-java.lang.String}
```
public static void convert(String inputFile, String outputFile)
```


Преобразует заданный входной документ в выходной документ, используя указанные имена входного и выходного файлов и их расширения.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

 **Examples:** 

Показывает, как преобразовать документы одной строкой кода.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | java.lang.String | Имя входного файла. |
| outputFile | java.lang.String | Имя выходного файла. |

### convert(String inputFile, String outputFile, SaveOptions saveOptions) {#convert-java.lang.String-java.lang.String-com.aspose.words.SaveOptions}
```
public static void convert(String inputFile, String outputFile, SaveOptions saveOptions)
```


Преобразует заданный входной документ в выходной документ, используя указанные имена входного и выходного файлов и параметры сохранения.

 **Remarks:** 

Если формат вывода — изображение (BMP, EMF, EPS, GIF, JPEG, PNG или WebP), каждая страница вывода будет сохранена в отдельный файл. Указанное имя выходного файла будет использовано для генерации имён файлов для каждой части по правилу: outputFile\_partIndex.extension.

Если формат вывода — TIFF, вывод будет сохранён в один многостраничный файл TIFF.

 **Examples:** 

Показывает, как преобразовать документы одной строкой кода.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | java.lang.String | Имя входного файла. |
| outputFile | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Параметры сохранения. |

### convert(String inputFile, String outputFile, int saveFormat) {#convert-java.lang.String-java.lang.String-int}
```
public static void convert(String inputFile, String outputFile, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | java.lang.String |  |
| outputFile | java.lang.String |  |
| saveFormat | int |  |

### convertToImages(Document doc, ImageSaveOptions saveOptions) {#convertToImages-com.aspose.words.Document-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(Document doc, ImageSaveOptions saveOptions)
```


Преобразует страницы указанного документа в изображения, используя указанные параметры сохранения, и возвращает массив потоков, содержащих изображения.

 **Examples:** 

Показывает, как преобразовать документ в поток изображений.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | Входной документ. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения изображения. |

**Returns:**
java.io.OutputStream[] — Возвращает массив потоков изображений. Потоки должны быть освобождены конечным пользователем.
### convertToImages(Document doc, int saveFormat) {#convertToImages-com.aspose.words.Document-int}
```
public static OutputStream[] convertToImages(Document doc, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| saveFormat | int |  |

**Returns:**
java.io.OutputStream[]
### convertToImages(InputStream inputStream, ImageSaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(InputStream inputStream, ImageSaveOptions saveOptions)
```


Преобразует страницы указанного входного потока в изображения, используя указанные параметры сохранения, и возвращает массив потоков, содержащих изображения.

 **Examples:** 

Показывает, как преобразовать документ в изображения из потока.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения изображения. |

**Returns:**
java.io.OutputStream[] — Возвращает массив потоков изображений. Потоки должны быть освобождены конечным пользователем.
### convertToImages(InputStream inputStream, LoadOptions loadOptions, ImageSaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(InputStream inputStream, LoadOptions loadOptions, ImageSaveOptions saveOptions)
```


Преобразует страницы указанного входного потока в изображения, используя предоставленные параметры загрузки и сохранения, и возвращает массив потоков, содержащих изображения.

 **Examples:** 

Показывает, как преобразовать документ в изображения из потока.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream | Входной поток. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Параметры загрузки входного документа. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения изображения. |

**Returns:**
java.io.OutputStream[] — Возвращает массив потоков изображений. Потоки должны быть освобождены конечным пользователем.
### convertToImages(InputStream inputStream, int saveFormat) {#convertToImages-java.io.InputStream-int}
```
public static OutputStream[] convertToImages(InputStream inputStream, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| saveFormat | int |  |

**Returns:**
java.io.OutputStream[]
### convertToImages(String inputFile, ImageSaveOptions saveOptions) {#convertToImages-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(String inputFile, ImageSaveOptions saveOptions)
```


Преобразует страницы указанного входного файла в изображения, используя указанные параметры сохранения, и возвращает массив потоков, содержащих изображения.

 **Examples:** 

Показывает, как преобразовать документ в поток изображений.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | java.lang.String | Имя входного файла. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения изображения. |

**Returns:**
java.io.OutputStream[] — Возвращает массив потоков изображений. Потоки должны быть освобождены конечным пользователем.
### convertToImages(String inputFile, LoadOptions loadOptions, String outputFile, ImageSaveOptions saveOptions) {#convertToImages-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public static void convertToImages(String inputFile, LoadOptions loadOptions, String outputFile, ImageSaveOptions saveOptions)
```


Преобразует страницы указанного входного файла в файлы изображений, используя предоставленные параметры загрузки и сохранения.

 **Examples:** 

Показывает, как преобразовать документ в изображения.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | java.lang.String | Имя входного файла. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Параметры загрузки входного документа. |
| outputFile | java.lang.String | Имя выходного файла, используемое для генерации имени файлов изображений страниц по правилу "outputFile\_pageIndex.extension" |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения изображения. |

### convertToImages(String inputFile, int saveFormat) {#convertToImages-java.lang.String-int}
```
public static OutputStream[] convertToImages(String inputFile, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
java.io.OutputStream[]
### convertToImages(String inputFile, String outputFile) {#convertToImages-java.lang.String-java.lang.String}
```
public static void convertToImages(String inputFile, String outputFile)
```


Преобразует страницы указанного входного файла в файлы изображений.

 **Examples:** 

Показывает, как преобразовать документ в изображения.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | java.lang.String | Имя входного файла. |
| outputFile | java.lang.String | Имя выходного файла, используемое для генерации имени файлов изображений страниц по правилу "outputFile\_pageIndex.extension" |

### convertToImages(String inputFile, String outputFile, ImageSaveOptions saveOptions) {#convertToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public static void convertToImages(String inputFile, String outputFile, ImageSaveOptions saveOptions)
```


Преобразует страницы указанного входного файла в файлы изображений, используя указанные параметры сохранения.

 **Examples:** 

Показывает, как преобразовать документ в изображения.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | java.lang.String | Имя входного файла. |
| outputFile | java.lang.String | Имя выходного файла, используемое для генерации имени файлов изображений страниц по правилу "outputFile\_pageIndex.extension" |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Параметры сохранения изображения. |

### convertToImages(String inputFile, String outputFile, int saveFormat) {#convertToImages-java.lang.String-java.lang.String-int}
```
public static void convertToImages(String inputFile, String outputFile, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| inputFile | java.lang.String |  |
| outputFile | java.lang.String |  |
| saveFormat | int |  |

### create() {#create}
```
public static Converter create()
```


Создаёт новый экземпляр процессора конвертера.

**Returns:**
[Converter](../../com.aspose.words/converter/)
### create(ConverterContext context) {#create-com.aspose.words.ConverterContext}
```
public static Converter create(ConverterContext context)
```


Создаёт новый экземпляр процессора конвертера.

 **Examples:** 

Показывает, как конвертировать документы одной строкой кода, используя контекст.

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

Показывает, как конвертировать документы из потока одной строкой кода, используя контекст.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| context | [ConverterContext](../../com.aspose.words/convertercontext/) |  |

**Returns:**
[Converter](../../com.aspose.words/converter/)
### execute() {#execute}
```
public void execute()
```


Выполнить действие процессора.

 **Examples:** 

Показывает, как объединить документы в один результирующий документ, используя контекст.

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

Показывает, как объединить документы из потока в один результирующий документ, используя контекст.

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

Показывает, как конвертировать документы одной строкой кода, используя контекст.

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

Показывает, как конвертировать документы из потока одной строкой кода, используя контекст.

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


Указывает входной документ для обработки.

 **Remarks:** 

Если процессор принимает в качестве входа только один файл, будет обработан только последний указанный файл. Процессор [Merger](../../com.aspose.words/merger/) принимает несколько файлов в качестве входа, в результате все указанные документы будут объединены. Процессор [Converter](../../com.aspose.words/converter/) принимает в качестве входа только один файл, поэтому будет преобразован только последний указанный файл.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ввод | java.io.InputStream | Поток входного документа. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


Указывает входной документ для обработки.

 **Remarks:** 

Если процессор принимает в качестве входа только один файл, будет обработан только последний указанный файл. Процессор [Merger](../../com.aspose.words/merger/) принимает несколько файлов в качестве входа, в результате все указанные документы будут объединены. Процессор [Converter](../../com.aspose.words/converter/) принимает в качестве входа только один файл, поэтому будет преобразован только последний указанный файл.

 **Examples:** 

Показывает, как объединить документы из потока в один результирующий документ, используя контекст.

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

Показывает, как конвертировать документы из потока одной строкой кода, используя контекст.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| ввод | java.io.InputStream | Поток входного документа. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Необязательные параметры загрузки, используемые для загрузки документа. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


Указывает входной документ для обработки.

 **Remarks:** 

Если процессор принимает в качестве входа только один файл, будет обработан только последний указанный файл. Процессор [Merger](../../com.aspose.words/merger/) принимает несколько файлов в качестве входа, в результате все указанные документы будут объединены. Процессор [Converter](../../com.aspose.words/converter/) принимает в качестве входа только один файл, поэтому будет преобразован только последний указанный файл.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| ввод | java.lang.String | Имя файла входного документа. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


Указывает входной документ для обработки.

 **Remarks:** 

Если процессор принимает в качестве входа только один файл, будет обработан только последний указанный файл. Процессор [Merger](../../com.aspose.words/merger/) принимает несколько файлов в качестве входа, в результате все указанные документы будут объединены. Процессор [Converter](../../com.aspose.words/converter/) принимает в качестве входа только один файл, поэтому будет преобразован только последний указанный файл.

 **Examples:** 

Показывает, как объединить документы в один результирующий документ, используя контекст.

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

Показывает, как конвертировать документы одной строкой кода, используя контекст.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| ввод | java.lang.String | Имя файла входного документа. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Необязательные параметры загрузки, используемые для загрузки документа. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


Указывает выходной файл для процессора.

 **Remarks:** 

Если вывод состоит из нескольких файлов, указанное имя выходного файла используется для генерации имени файла каждой части по правилу: 'outputFile\_partIndex.extension'.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.lang.String | Имя выходного файла. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


Указывает выходной файл для процессора.

 **Remarks:** 

Если вывод состоит из нескольких файлов, указанное имя выходного файла используется для генерации имени файла каждой части по правилу: 'outputFile\_partIndex.extension'.

 **Examples:** 

Показывает, как объединить документы в один результирующий документ, используя контекст.

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

Показывает, как конвертировать документы одной строкой кода, используя контекст.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.lang.String | Имя выходного файла. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Необязательные параметры сохранения. Если не указано, формат сохраняемого файла определяется расширением. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| вывод | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
