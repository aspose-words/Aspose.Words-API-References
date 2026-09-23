---
title: "Converter"
linktitle: "Converter"
second_title: "Aspose.Words per Java"
description: "Rappresenta un gruppo di metodi destinati a convertire una varietà di diversi tipi di documenti utilizzando una singola riga di codice in Java."
type: docs
weight: 132
url: /it/java/com.aspose.words/converter/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Converter extends Processor
```

Rappresenta un gruppo di metodi destinati a convertire una varietà di diversi tipi di documenti usando una singola riga di codice.

 **Remarks:** 

I file o i flussi di input e output specificati, insieme al formato di salvataggio desiderato, vengono utilizzati per convertire il documento di input fornito da un formato nel documento di output dell'altro formato specificato.

La funzionalità di conversione supporta oltre 35 diversi formati di file.

Il gruppo di metodi **M:Aspose.Words.LowCode.Converter.ConvertToImages(System.String,Aspose.Words.SaveFormat)** è progettato per trasformare i documenti in immagini, con ogni pagina convertita in un file immagine separato. Questi metodi convertono anche i documenti PDF direttamente in formati a pagina fissa senza caricarli nel modello del documento, migliorando sia le prestazioni che l'accuratezza.

Con [ImageSaveOptions.getPageSet()](../../com.aspose.words/imagesaveoptions/\#getPageSet) / [ImageSaveOptions.setPageSet(com.aspose.words.PageSet)](../../com.aspose.words/imagesaveoptions/\#setPageSet-com.aspose.words.PageSet), è possibile specificare un insieme particolare di pagine da convertire in immagini.
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [convert(InputStream inputStream, LoadOptions loadOptions, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-com.aspose.words.LoadOptions-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convert(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions)](#convert-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [convert(InputStream inputStream, OutputStream outputStream, int saveFormat)](#convert-java.io.InputStream-java.io.OutputStream-int) |  |
| [convert(String inputFile, LoadOptions loadOptions, String outputFile, SaveOptions saveOptions)](#convert-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.SaveOptions) | Converte il documento di input fornito nel documento di output utilizzando i nomi di file di input e output specificati e le relative opzioni di caricamento/salvataggio. |
| [convert(String inputFile, String outputFile)](#convert-java.lang.String-java.lang.String) | Converte il documento di input fornito nel documento di output usando i nomi di file di input e output specificati e le relative estensioni. |
| [convert(String inputFile, String outputFile, SaveOptions saveOptions)](#convert-java.lang.String-java.lang.String-com.aspose.words.SaveOptions) | Converte il documento di input fornito nel documento di output usando i nomi di file di input e output specificati e le opzioni di salvataggio. |
| [convert(String inputFile, String outputFile, int saveFormat)](#convert-java.lang.String-java.lang.String-int) |  |
| [convertToImages(Document doc, ImageSaveOptions saveOptions)](#convertToImages-com.aspose.words.Document-com.aspose.words.ImageSaveOptions) | Converte le pagine del documento specificato in immagini usando le opzioni di salvataggio specificate e restituisce un array di stream contenenti le immagini. |
| [convertToImages(Document doc, int saveFormat)](#convertToImages-com.aspose.words.Document-int) |  |
| [convertToImages(InputStream inputStream, ImageSaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions) | Converte le pagine dello stream di input specificato in immagini usando le opzioni di salvataggio specificate e restituisce un array di stream contenenti le immagini. |
| [convertToImages(InputStream inputStream, LoadOptions loadOptions, ImageSaveOptions saveOptions)](#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.ImageSaveOptions) | Converte le pagine dello stream di input specificato in immagini usando le opzioni di caricamento e salvataggio fornite, e restituisce un array di stream contenenti le immagini. |
| [convertToImages(InputStream inputStream, int saveFormat)](#convertToImages-java.io.InputStream-int) |  |
| [convertToImages(String inputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-com.aspose.words.ImageSaveOptions) | Converte le pagine del file di input specificato in immagini usando le opzioni di salvataggio specificate e restituisce un array di stream contenenti le immagini. |
| [convertToImages(String inputFile, LoadOptions loadOptions, String outputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.ImageSaveOptions) | Converte le pagine del file di input specificato in file immagine usando le opzioni di caricamento e salvataggio fornite. |
| [convertToImages(String inputFile, int saveFormat)](#convertToImages-java.lang.String-int) |  |
| [convertToImages(String inputFile, String outputFile)](#convertToImages-java.lang.String-java.lang.String) | Converte le pagine del file di input specificato in file immagine. |
| [convertToImages(String inputFile, String outputFile, ImageSaveOptions saveOptions)](#convertToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions) | Converte le pagine del file di input specificato in file immagine usando le opzioni di salvataggio specificate. |
| [convertToImages(String inputFile, String outputFile, int saveFormat)](#convertToImages-java.lang.String-java.lang.String-int) |  |
| [create()](#create) | Crea una nuova istanza del processore di conversione. |
| [create(ConverterContext context)](#create-com.aspose.words.ConverterContext) | Crea una nuova istanza del processore di conversione. |
| [execute()](#execute) | Esegui l'azione del processore. |
| [from(InputStream input)](#from-java.io.InputStream) | Specifica il documento di input per l'elaborazione. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Specifica il documento di input per l'elaborazione. |
| [from(String input)](#from-java.lang.String) | Specifica il documento di input per l'elaborazione. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Specifica il documento di input per l'elaborazione. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Specifica il file di output per il processore. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Specifica il file di output per il processore. |
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
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

### convert(InputStream inputStream, OutputStream outputStream, int saveFormat) {#convert-java.io.InputStream-java.io.OutputStream-int}
```
public static void convert(InputStream inputStream, OutputStream outputStream, int saveFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |

### convert(String inputFile, LoadOptions loadOptions, String outputFile, SaveOptions saveOptions) {#convert-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.SaveOptions}
```
public static void convert(String inputFile, LoadOptions loadOptions, String outputFile, SaveOptions saveOptions)
```


Converte il documento di input fornito nel documento di output utilizzando i nomi di file di input e output specificati e le relative opzioni di caricamento/salvataggio.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

 **Examples:** 

Mostra come convertire i documenti con una singola riga di codice.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | java.lang.String | Il nome file di input. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Le opzioni di caricamento del documento di input. |
| outputFile | java.lang.String | Il nome file di output. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Le opzioni di salvataggio. |

### convert(String inputFile, String outputFile) {#convert-java.lang.String-java.lang.String}
```
public static void convert(String inputFile, String outputFile)
```


Converte il documento di input fornito nel documento di output usando i nomi di file di input e output specificati e le relative estensioni.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

 **Examples:** 

Mostra come convertire i documenti con una singola riga di codice.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | java.lang.String | Il nome file di input. |
| outputFile | java.lang.String | Il nome file di output. |

### convert(String inputFile, String outputFile, SaveOptions saveOptions) {#convert-java.lang.String-java.lang.String-com.aspose.words.SaveOptions}
```
public static void convert(String inputFile, String outputFile, SaveOptions saveOptions)
```


Converte il documento di input fornito nel documento di output usando i nomi di file di input e output specificati e le opzioni di salvataggio.

 **Remarks:** 

Se il formato di output è un'immagine (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), ogni pagina dell'output verrà salvata come file separato. Il nome file di output specificato verrà utilizzato per generare i nomi file per ogni parte seguendo la regola: outputFile\_partIndex.extension.

Se il formato di output è TIFF, l'output verrà salvato come un unico file TIFF multi-frame.

 **Examples:** 

Mostra come convertire i documenti con una singola riga di codice.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | java.lang.String | Il nome file di input. |
| outputFile | java.lang.String | Il nome file di output. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Le opzioni di salvataggio. |

### convert(String inputFile, String outputFile, int saveFormat) {#convert-java.lang.String-java.lang.String-int}
```
public static void convert(String inputFile, String outputFile, int saveFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | java.lang.String |  |
| outputFile | java.lang.String |  |
| saveFormat | int |  |

### convertToImages(Document doc, ImageSaveOptions saveOptions) {#convertToImages-com.aspose.words.Document-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(Document doc, ImageSaveOptions saveOptions)
```


Converte le pagine del documento specificato in immagini usando le opzioni di salvataggio specificate e restituisce un array di stream contenenti le immagini.

 **Examples:** 

Mostra come convertire il documento in un flusso di immagini.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) | Il documento di input. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Opzioni di salvataggio dell'immagine. |

**Returns:**
java.io.OutputStream[] - Restituisce un array di stream di immagini. Gli stream devono essere eliminati dall'utente finale.
### convertToImages(Document doc, int saveFormat) {#convertToImages-com.aspose.words.Document-int}
```
public static OutputStream[] convertToImages(Document doc, int saveFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document/) |  |
| saveFormat | int |  |

**Returns:**
java.io.OutputStream[]
### convertToImages(InputStream inputStream, ImageSaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(InputStream inputStream, ImageSaveOptions saveOptions)
```


Converte le pagine dello stream di input specificato in immagini usando le opzioni di salvataggio specificate e restituisce un array di stream contenenti le immagini.

 **Examples:** 

Mostra come convertire il documento in immagini dallo stream.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | java.io.InputStream | Il flusso di input. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Opzioni di salvataggio dell'immagine. |

**Returns:**
java.io.OutputStream[] - Restituisce un array di stream di immagini. Gli stream devono essere eliminati dall'utente finale.
### convertToImages(InputStream inputStream, LoadOptions loadOptions, ImageSaveOptions saveOptions) {#convertToImages-java.io.InputStream-com.aspose.words.LoadOptions-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(InputStream inputStream, LoadOptions loadOptions, ImageSaveOptions saveOptions)
```


Converte le pagine dello stream di input specificato in immagini usando le opzioni di caricamento e salvataggio fornite, e restituisce un array di stream contenenti le immagini.

 **Examples:** 

Mostra come convertire il documento in immagini dallo stream.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | java.io.InputStream | Il flusso di input. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Le opzioni di caricamento del documento di input. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Opzioni di salvataggio dell'immagine. |

**Returns:**
java.io.OutputStream[] - Restituisce un array di stream di immagini. Gli stream devono essere eliminati dall'utente finale.
### convertToImages(InputStream inputStream, int saveFormat) {#convertToImages-java.io.InputStream-int}
```
public static OutputStream[] convertToImages(InputStream inputStream, int saveFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| saveFormat | int |  |

**Returns:**
java.io.OutputStream[]
### convertToImages(String inputFile, ImageSaveOptions saveOptions) {#convertToImages-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public static OutputStream[] convertToImages(String inputFile, ImageSaveOptions saveOptions)
```


Converte le pagine del file di input specificato in immagini usando le opzioni di salvataggio specificate e restituisce un array di stream contenenti le immagini.

 **Examples:** 

Mostra come convertire il documento in un flusso di immagini.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | java.lang.String | Il nome file di input. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Opzioni di salvataggio dell'immagine. |

**Returns:**
java.io.OutputStream[] - Restituisce un array di stream di immagini. Gli stream devono essere eliminati dall'utente finale.
### convertToImages(String inputFile, LoadOptions loadOptions, String outputFile, ImageSaveOptions saveOptions) {#convertToImages-java.lang.String-com.aspose.words.LoadOptions-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public static void convertToImages(String inputFile, LoadOptions loadOptions, String outputFile, ImageSaveOptions saveOptions)
```


Converte le pagine del file di input specificato in file immagine usando le opzioni di caricamento e salvataggio fornite.

 **Examples:** 

Mostra come convertire il documento in immagini.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | java.lang.String | Il nome file di input. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Le opzioni di caricamento del documento di input. |
| outputFile | java.lang.String | Il nome file di output utilizzato per generare il nome file per le immagini delle pagine usando la regola "outputFile\_pageIndex.extension" |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Opzioni di salvataggio dell'immagine. |

### convertToImages(String inputFile, int saveFormat) {#convertToImages-java.lang.String-int}
```
public static OutputStream[] convertToImages(String inputFile, int saveFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
java.io.OutputStream[]
### convertToImages(String inputFile, String outputFile) {#convertToImages-java.lang.String-java.lang.String}
```
public static void convertToImages(String inputFile, String outputFile)
```


Converte le pagine del file di input specificato in file immagine.

 **Examples:** 

Mostra come convertire il documento in immagini.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | java.lang.String | Il nome file di input. |
| outputFile | java.lang.String | Il nome file di output utilizzato per generare il nome file per le immagini delle pagine usando la regola "outputFile\_pageIndex.extension" |

### convertToImages(String inputFile, String outputFile, ImageSaveOptions saveOptions) {#convertToImages-java.lang.String-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public static void convertToImages(String inputFile, String outputFile, ImageSaveOptions saveOptions)
```


Converte le pagine del file di input specificato in file immagine usando le opzioni di salvataggio specificate.

 **Examples:** 

Mostra come convertire il documento in immagini.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | java.lang.String | Il nome file di input. |
| outputFile | java.lang.String | Il nome file di output utilizzato per generare il nome file per le immagini delle pagine usando la regola "outputFile\_pageIndex.extension" |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Opzioni di salvataggio dell'immagine. |

### convertToImages(String inputFile, String outputFile, int saveFormat) {#convertToImages-java.lang.String-java.lang.String-int}
```
public static void convertToImages(String inputFile, String outputFile, int saveFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFile | java.lang.String |  |
| outputFile | java.lang.String |  |
| saveFormat | int |  |

### create() {#create}
```
public static Converter create()
```


Crea una nuova istanza del processore di conversione.

**Returns:**
[Converter](../../com.aspose.words/converter/)
### create(ConverterContext context) {#create-com.aspose.words.ConverterContext}
```
public static Converter create(ConverterContext context)
```


Crea una nuova istanza del processore di conversione.

 **Examples:** 

Mostra come convertire documenti con una singola riga di codice usando il contesto.

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

Mostra come convertire documenti dallo stream con una singola riga di codice usando il contesto.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| context | [ConverterContext](../../com.aspose.words/convertercontext/) |  |

**Returns:**
[Converter](../../com.aspose.words/converter/)
### execute() {#execute}
```
public void execute()
```


Esegui l'azione del processore.

 **Examples:** 

Mostra come unire documenti in un unico documento di output usando il contesto.

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

Mostra come unire documenti dallo stream in un unico documento di output usando il contesto.

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

Mostra come convertire documenti con una singola riga di codice usando il contesto.

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

Mostra come convertire documenti dallo stream con una singola riga di codice usando il contesto.

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


Specifica il documento di input per l'elaborazione.

 **Remarks:** 

Se il processore accetta solo un file come input, verrà elaborato solo l'ultimo file specificato. Il processore [Merger](../../com.aspose.words/merger/) accetta più file come input, quindi tutti i documenti specificati verranno uniti. Il processore [Converter](../../com.aspose.words/converter/) accetta solo un file come input, quindi solo l'ultimo file specificato verrà convertito.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| input | java.io.InputStream | Stream del documento di input. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


Specifica il documento di input per l'elaborazione.

 **Remarks:** 

Se il processore accetta solo un file come input, verrà elaborato solo l'ultimo file specificato. Il processore [Merger](../../com.aspose.words/merger/) accetta più file come input, quindi tutti i documenti specificati verranno uniti. Il processore [Converter](../../com.aspose.words/converter/) accetta solo un file come input, quindi solo l'ultimo file specificato verrà convertito.

 **Examples:** 

Mostra come unire documenti dallo stream in un unico documento di output usando il contesto.

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

Mostra come convertire documenti dallo stream con una singola riga di codice usando il contesto.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| input | java.io.InputStream | Stream del documento di input. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Opzioni di caricamento opzionali usate per caricare il documento. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


Specifica il documento di input per l'elaborazione.

 **Remarks:** 

Se il processore accetta solo un file come input, verrà elaborato solo l'ultimo file specificato. Il processore [Merger](../../com.aspose.words/merger/) accetta più file come input, quindi tutti i documenti specificati verranno uniti. Il processore [Converter](../../com.aspose.words/converter/) accetta solo un file come input, quindi solo l'ultimo file specificato verrà convertito.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| input | java.lang.String | Nome file del documento di input. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


Specifica il documento di input per l'elaborazione.

 **Remarks:** 

Se il processore accetta solo un file come input, verrà elaborato solo l'ultimo file specificato. Il processore [Merger](../../com.aspose.words/merger/) accetta più file come input, quindi tutti i documenti specificati verranno uniti. Il processore [Converter](../../com.aspose.words/converter/) accetta solo un file come input, quindi solo l'ultimo file specificato verrà convertito.

 **Examples:** 

Mostra come unire documenti in un unico documento di output usando il contesto.

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

Mostra come convertire documenti con una singola riga di codice usando il contesto.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| input | java.lang.String | Nome file del documento di input. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Opzioni di caricamento opzionali usate per caricare il documento. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


Specifica il file di output per il processore.

 **Remarks:** 

Se l'output consiste di più file, il nome file di output specificato viene usato per generare il nome file per ogni parte secondo la regola: 'outputFile\_partIndex.extension'.

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.lang.String | Nome file di output. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


Specifica il file di output per il processore.

 **Remarks:** 

Se l'output consiste di più file, il nome file di output specificato viene usato per generare il nome file per ogni parte secondo la regola: 'outputFile\_partIndex.extension'.

 **Examples:** 

Mostra come unire documenti in un unico documento di output usando il contesto.

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

Mostra come convertire documenti con una singola riga di codice usando il contesto.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.lang.String | Nome file di output. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Opzioni di salvataggio opzionali. Se non specificate, il formato di salvataggio è determinato dall'estensione del file. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| output | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
