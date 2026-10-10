---
title: "Watermarker"
linktitle: "Watermarker"
second_title: "Aspose.Words pour Java"
description: "Fournit des méthodes destinées à insérer des filigranes dans les documents en Java."
type: docs
weight: 724
url: /fr/java/com.aspose.words/watermarker/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Watermarker extends Processor
```

Fournit des méthodes destinées à insérer des filigranes dans les documents.
## Méthodes

| Méthode | Description |
| --- | --- |
| [create(WatermarkerContext context)](#create-com.aspose.words.WatermarkerContext) | Crée une nouvelle instance du processeur de filigrane. |
| [execute()](#execute) | Exécute l'action du processeur. |
| [from(InputStream input)](#from-java.io.InputStream) | Spécifie le document d'entrée pour le traitement. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Spécifie le document d'entrée pour le traitement. |
| [from(String input)](#from-java.lang.String) | Spécifie le document d'entrée pour le traitement. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Spécifie le document d'entrée pour le traitement. |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.io.InputStream) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.awt.image.BufferedImage) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.io.InputStream) |  |
| [setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream, ImageWatermarkOptions options)](#setImage-java.io.InputStream-java.io.OutputStream-int-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName)](#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String) | Ajoute un filigrane image dans le document avec des options et le format d'enregistrement spécifié. |
| [setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName, ImageWatermarkOptions options)](#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.ImageWatermarkOptions) | Ajoute un filigrane image dans le document avec des options et le format d'enregistrement spécifié. |
| [setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName)](#setImage-java.lang.String-java.lang.String-int-java.lang.String) |  |
| [setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName, ImageWatermarkOptions options)](#setImage-java.lang.String-java.lang.String-int-java.lang.String-com.aspose.words.ImageWatermarkOptions) |  |
| [setImage(String inputFileName, String outputFileName, String watermarkImageFileName)](#setImage-java.lang.String-java.lang.String-java.lang.String) | Ajoute un filigrane image dans le document. |
| [setImage(String inputFileName, String outputFileName, String watermarkImageFileName, ImageWatermarkOptions options)](#setImage-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.ImageWatermarkOptions) | Ajoute un filigrane image dans le document avec des options. |
| [setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText)](#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String) |  |
| [setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) |  |
| [setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText)](#setText-java.io.InputStream-java.io.OutputStream-int-java.lang.String) |  |
| [setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText, TextWatermarkOptions options)](#setText-java.io.InputStream-java.io.OutputStream-int-java.lang.String-com.aspose.words.TextWatermarkOptions) |  |
| [setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText)](#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String) | Ajoute un filigrane texte dans le document avec des options et le format d'enregistrement spécifié. |
| [setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) | Ajoute un filigrane texte dans le document avec des options et le format d'enregistrement spécifié. |
| [setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText)](#setText-java.lang.String-java.lang.String-int-java.lang.String) |  |
| [setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText, TextWatermarkOptions options)](#setText-java.lang.String-java.lang.String-int-java.lang.String-com.aspose.words.TextWatermarkOptions) |  |
| [setText(String inputFileName, String outputFileName, String watermarkText)](#setText-java.lang.String-java.lang.String-java.lang.String) | Ajoute un filigrane texte dans le document. |
| [setText(String inputFileName, String outputFileName, String watermarkText, TextWatermarkOptions options)](#setText-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.TextWatermarkOptions) | Ajoute un filigrane texte dans le document avec des options. |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream) | Ajoute un filigrane image dans le document avec des options. |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions) | Ajoute un filigrane image dans le document avec des options. |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String) | Ajoute un filigrane texte dans le document avec des options. |
| [setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) | Ajoute un filigrane texte dans le document avec des options. |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte) | Ajoute un filigrane image dans le document avec des options. |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes, ImageWatermarkOptions options)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte---com.aspose.words.ImageWatermarkOptions) | Ajoute un filigrane image dans le document avec des options. |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String) | Ajoute un filigrane texte dans le document avec des options. |
| [setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)](#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions) | Ajoute un filigrane texte dans le document avec des options. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Spécifie le fichier de sortie pour le processeur. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Spécifie le fichier de sortie pour le processeur. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(WatermarkerContext context) {#create-com.aspose.words.WatermarkerContext}
```
public static Watermarker create(WatermarkerContext context)
```


Crée une nouvelle instance du processeur de filigrane.

 **Examples:** 

Montre comment insérer du texte de filigrane dans le document en utilisant le contexte.

```

 String doc = getMyDir() + "Big document.docx";
 String watermarkText = "This is a watermark";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setTextWatermark(watermarkText);

 watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextText.docx")
         .execute();
 
```

Montre comment insérer du texte de filigrane dans le document depuis le flux en utilisant le contexte.

```

 String watermarkText = "This is a watermark";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setTextWatermark(watermarkText);

     watermarkerContext.getTextWatermarkOptions().setColor(Color.RED);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextTextStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

Montre comment insérer une image de filigrane dans le document en utilisant le contexte.

```

 String doc = getMyDir() + "Document.docx";
 String watermarkImage = getImageDir() + "Logo.jpg";

 WatermarkerContext watermarkerContext = new WatermarkerContext();
 watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

 watermarkerContext.getImageWatermarkOptions().setScale(50.0);

 Watermarker.create(watermarkerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.WatermarkContextImage.docx")
         .execute();
 
```

Montre comment insérer une image de filigrane dans le document depuis un flux en utilisant le contexte.

```

 String watermarkImage = getImageDir() + "Logo.jpg";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     WatermarkerContext watermarkerContext = new WatermarkerContext();
     watermarkerContext.setImageWatermark(Files.readAllBytes(Paths.get(watermarkImage)));

     watermarkerContext.getImageWatermarkOptions().setScale(50.0);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.WatermarkContextImageStream.docx")) {
         Watermarker.create(watermarkerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| context | [WatermarkerContext](../../com.aspose.words/watermarkercontext/) |  |

**Returns:**
[Watermarker](../../com.aspose.words/watermarker/)
### execute() {#execute}
```
public void execute()
```


Exécute l'action du processeur.

 **Examples:** 

Montre comment fusionner des documents en un seul document de sortie en utilisant le contexte.

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

Montre comment fusionner des documents du flux en un seul document de sortie en utilisant le contexte.

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

Montre comment convertir des documents avec une seule ligne de code en utilisant le contexte.

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

Montre comment convertir des documents du flux avec une seule ligne de code en utilisant le contexte.

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


Spécifie le document d'entrée pour le traitement.

 **Remarks:** 

Si le processeur n'accepte qu'un seul fichier en entrée, seul le dernier fichier spécifié sera traité. Le processeur [Merger](../../com.aspose.words/merger/) accepte plusieurs fichiers en entrée, de sorte que tous les documents spécifiés seront fusionnés. Le processeur [Converter](../../com.aspose.words/converter/) n'accepte qu'un seul fichier en entrée, ainsi le dernier fichier spécifié sera converti.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| entrée | java.io.InputStream | Flux du document d'entrée. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


Spécifie le document d'entrée pour le traitement.

 **Remarks:** 

Si le processeur n'accepte qu'un seul fichier en entrée, seul le dernier fichier spécifié sera traité. Le processeur [Merger](../../com.aspose.words/merger/) accepte plusieurs fichiers en entrée, de sorte que tous les documents spécifiés seront fusionnés. Le processeur [Converter](../../com.aspose.words/converter/) n'accepte qu'un seul fichier en entrée, ainsi le dernier fichier spécifié sera converti.

 **Examples:** 

Montre comment fusionner des documents du flux en un seul document de sortie en utilisant le contexte.

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

Montre comment convertir des documents du flux avec une seule ligne de code en utilisant le contexte.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| entrée | java.io.InputStream | Flux du document d'entrée. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Options de chargement facultatives utilisées pour charger le document. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


Spécifie le document d'entrée pour le traitement.

 **Remarks:** 

Si le processeur n'accepte qu'un seul fichier en entrée, seul le dernier fichier spécifié sera traité. Le processeur [Merger](../../com.aspose.words/merger/) accepte plusieurs fichiers en entrée, de sorte que tous les documents spécifiés seront fusionnés. Le processeur [Converter](../../com.aspose.words/converter/) n'accepte qu'un seul fichier en entrée, ainsi le dernier fichier spécifié sera converti.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| entrée | java.lang.String | Nom de fichier du document d'entrée. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


Spécifie le document d'entrée pour le traitement.

 **Remarks:** 

Si le processeur n'accepte qu'un seul fichier en entrée, seul le dernier fichier spécifié sera traité. Le processeur [Merger](../../com.aspose.words/merger/) accepte plusieurs fichiers en entrée, de sorte que tous les documents spécifiés seront fusionnés. Le processeur [Converter](../../com.aspose.words/converter/) n'accepte qu'un seul fichier en entrée, ainsi le dernier fichier spécifié sera converti.

 **Examples:** 

Montre comment fusionner des documents en un seul document de sortie en utilisant le contexte.

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

Montre comment convertir des documents avec une seule ligne de code en utilisant le contexte.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| entrée | java.lang.String | Nom de fichier du document d'entrée. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Options de chargement facultatives utilisées pour charger le document. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage) {#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| watermarkImage | java.awt.image.BufferedImage |  |

### setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage, ImageWatermarkOptions options) {#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, BufferedImage watermarkImage, ImageWatermarkOptions options)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| watermarkImage | java.awt.image.BufferedImage |  |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) |  |

### setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream) {#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.io.InputStream}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| watermarkImageStream | java.io.InputStream |  |

### setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options) {#setImage-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| watermarkImageStream | java.io.InputStream |  |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) |  |

### setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage) {#setImage-java.io.InputStream-java.io.OutputStream-int-java.awt.image.BufferedImage}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| watermarkImage | java.awt.image.BufferedImage |  |

### setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage, ImageWatermarkOptions options) {#setImage-java.io.InputStream-java.io.OutputStream-int-java.awt.image.BufferedImage-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, BufferedImage watermarkImage, ImageWatermarkOptions options)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| watermarkImage | java.awt.image.BufferedImage |  |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) |  |

### setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream) {#setImage-java.io.InputStream-java.io.OutputStream-int-java.io.InputStream}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| watermarkImageStream | java.io.InputStream |  |

### setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream, ImageWatermarkOptions options) {#setImage-java.io.InputStream-java.io.OutputStream-int-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(InputStream inputStream, OutputStream outputStream, int saveFormat, InputStream watermarkImageStream, ImageWatermarkOptions options)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| watermarkImageStream | java.io.InputStream |  |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) |  |

### setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName) {#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String}
```
public static void setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName)
```


Ajoute un filigrane image dans le document avec des options et le format d'enregistrement spécifié.

 **Remarks:** 

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile\_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée dans un seul fichier TIFF multi‑images.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| outputFileName | java.lang.String | Le nom de fichier de sortie. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Les options d'enregistrement. |
| watermarkImageFileName | java.lang.String | Image affichée comme filigrane. |

### setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName, ImageWatermarkOptions options) {#setImage-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkImageFileName, ImageWatermarkOptions options)
```


Ajoute un filigrane image dans le document avec des options et le format d'enregistrement spécifié.

 **Remarks:** 

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile\_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée dans un seul fichier TIFF multi‑images.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| outputFileName | java.lang.String | Le nom de fichier de sortie. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Les options d'enregistrement. |
| watermarkImageFileName | java.lang.String | Image affichée comme filigrane. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Définit des options supplémentaires pour le filigrane image. |

### setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName) {#setImage-java.lang.String-java.lang.String-int-java.lang.String}
```
public static void setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| watermarkImageFileName | java.lang.String |  |

### setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName, ImageWatermarkOptions options) {#setImage-java.lang.String-java.lang.String-int-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(String inputFileName, String outputFileName, int saveFormat, String watermarkImageFileName, ImageWatermarkOptions options)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| watermarkImageFileName | java.lang.String |  |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) |  |

### setImage(String inputFileName, String outputFileName, String watermarkImageFileName) {#setImage-java.lang.String-java.lang.String-java.lang.String}
```
public static void setImage(String inputFileName, String outputFileName, String watermarkImageFileName)
```


Ajoute un filigrane image dans le document.

 **Remarks:** 

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile\_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée dans un seul fichier TIFF multi‑images.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| outputFileName | java.lang.String | Le nom de fichier de sortie. |
| watermarkImageFileName | java.lang.String | Image affichée comme filigrane. |

### setImage(String inputFileName, String outputFileName, String watermarkImageFileName, ImageWatermarkOptions options) {#setImage-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.ImageWatermarkOptions}
```
public static void setImage(String inputFileName, String outputFileName, String watermarkImageFileName, ImageWatermarkOptions options)
```


Ajoute un filigrane image dans le document avec des options.

 **Remarks:** 

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile\_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée dans un seul fichier TIFF multi‑images.

 **Examples:** 

Montre comment insérer une image de filigrane dans le document.

```

 String doc = getMyDir() + "Document.docx";
 String watermarkImage = getImageDir() + "Logo.jpg";

 Watermarker.setImage(doc, getArtifactsDir() + "LowCode.SetWatermarkImage.1.docx", watermarkImage);
 Watermarker.setImage(doc, getArtifactsDir() + "LowCode.SetWatermarkText.2.docx", SaveFormat.DOCX, watermarkImage);
 ImageWatermarkOptions options = new ImageWatermarkOptions();
 options.setScale(50.0);
 Watermarker.setImage(doc, getArtifactsDir() + "LowCode.SetWatermarkText.3.docx", watermarkImage, options);
 Watermarker.setImage(doc, getArtifactsDir() + "LowCode.SetWatermarkText.4.docx", SaveFormat.DOCX, watermarkImage, options);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| outputFileName | java.lang.String | Le nom de fichier de sortie. |
| watermarkImageFileName | java.lang.String | Image affichée comme filigrane. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Définit des options supplémentaires pour le filigrane image. |

### setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText) {#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String}
```
public static void setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| watermarkText | java.lang.String |  |

### setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setText-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static void setText(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| watermarkText | java.lang.String |  |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) |  |

### setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText) {#setText-java.io.InputStream-java.io.OutputStream-int-java.lang.String}
```
public static void setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| watermarkText | java.lang.String |  |

### setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText, TextWatermarkOptions options) {#setText-java.io.InputStream-java.io.OutputStream-int-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static void setText(InputStream inputStream, OutputStream outputStream, int saveFormat, String watermarkText, TextWatermarkOptions options)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| watermarkText | java.lang.String |  |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) |  |

### setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText) {#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String}
```
public static void setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText)
```


Ajoute un filigrane texte dans le document avec des options et le format d'enregistrement spécifié.

 **Remarks:** 

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile\_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée dans un seul fichier TIFF multi‑images.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| outputFileName | java.lang.String | Le nom de fichier de sortie. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Les options d'enregistrement. |
| watermarkText | java.lang.String | Texte affiché comme filigrane. |

### setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setText-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static void setText(String inputFileName, String outputFileName, SaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```


Ajoute un filigrane texte dans le document avec des options et le format d'enregistrement spécifié.

 **Remarks:** 

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile\_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée dans un seul fichier TIFF multi‑images.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| outputFileName | java.lang.String | Le nom de fichier de sortie. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Les options d'enregistrement. |
| watermarkText | java.lang.String | Texte affiché comme filigrane. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Définit des options supplémentaires pour le filigrane texte. |

### setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText) {#setText-java.lang.String-java.lang.String-int-java.lang.String}
```
public static void setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| watermarkText | java.lang.String |  |

### setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText, TextWatermarkOptions options) {#setText-java.lang.String-java.lang.String-int-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static void setText(String inputFileName, String outputFileName, int saveFormat, String watermarkText, TextWatermarkOptions options)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| watermarkText | java.lang.String |  |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) |  |

### setText(String inputFileName, String outputFileName, String watermarkText) {#setText-java.lang.String-java.lang.String-java.lang.String}
```
public static void setText(String inputFileName, String outputFileName, String watermarkText)
```


Ajoute un filigrane texte dans le document.

 **Remarks:** 

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile\_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée dans un seul fichier TIFF multi‑images.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| outputFileName | java.lang.String | Le nom de fichier de sortie. |
| watermarkText | java.lang.String | Texte affiché comme filigrane. |

### setText(String inputFileName, String outputFileName, String watermarkText, TextWatermarkOptions options) {#setText-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static void setText(String inputFileName, String outputFileName, String watermarkText, TextWatermarkOptions options)
```


Ajoute un filigrane texte dans le document avec des options.

 **Remarks:** 

Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile\_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée dans un seul fichier TIFF multi‑images.

 **Examples:** 

Montre comment insérer du texte de filigrane dans le document.

```

 String doc = getMyDir() + "Big document.docx";
 String watermarkText = "This is a watermark";

 Watermarker.setText(doc, getArtifactsDir() + "LowCode.WatermarkText.1.docx", watermarkText);
 Watermarker.setText(doc, getArtifactsDir() + "LowCode.WatermarkText.2.docx", SaveFormat.DOCX, watermarkText);
 TextWatermarkOptions options = new TextWatermarkOptions();
 options.setColor(Color.RED);
 Watermarker.setText(doc, getArtifactsDir() + "LowCode.WatermarkText.3.docx", watermarkText, options);
 Watermarker.setText(doc, getArtifactsDir() + "LowCode.WatermarkText.4.docx", SaveFormat.DOCX, watermarkText, options);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| outputFileName | java.lang.String | Le nom de fichier de sortie. |
| watermarkText | java.lang.String | Texte affiché comme filigrane. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Définit des options supplémentaires pour le filigrane texte. |

### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream)
```


Ajoute un filigrane image dans le document avec des options. Rend la sortie en images.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | Le flux d'entrée. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Les options d'enregistrement. |
| watermarkImageStream | java.io.InputStream | Flux d'image affiché comme filigrane. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.io.InputStream-com.aspose.words.ImageWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, InputStream watermarkImageStream, ImageWatermarkOptions options)
```


Ajoute un filigrane image dans le document avec des options. Rend la sortie en images.

 **Examples:** 

Montre comment insérer une image de filigrane dans le document depuis un flux et enregistrer le résultat en images.

```

 String watermarkImage = getImageDir() + "Logo.jpg";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     try (FileInputStream imageStream = new FileInputStream(watermarkImage)) {
         Watermarker.setWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), imageStream);
         ImageWatermarkOptions options = new ImageWatermarkOptions();
         options.setScale(50.0);
         Watermarker.setWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), imageStream, options);
     }
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | Le flux d'entrée. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Les options d'enregistrement. |
| watermarkImageStream | java.io.InputStream | Flux d'image affiché comme filigrane. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Définit des options supplémentaires pour le filigrane image. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText)
```


Ajoute un filigrane texte dans le document avec des options. Rend la sortie en images.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | Le flux de fichier d'entrée. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Les options d'enregistrement. |
| watermarkText | java.lang.String | Texte affiché comme filigrane. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setWatermarkToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(InputStream inputStream, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```


Ajoute un filigrane texte dans le document avec des options. Rend la sortie en images.

 **Examples:** 

Montre comment insérer du texte de filigrane dans le document depuis le flux et enregistrer le résultat en images.

```

 String watermarkText = "This is a watermark";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Document.docx")) {
     OutputStream[] images = Watermarker.setWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), watermarkText);

     TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
     watermarkOptions.setColor(Color.RED);
     images = Watermarker.setWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), watermarkText, watermarkOptions);
 }
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | java.io.InputStream | Le flux de fichier d'entrée. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Les options d'enregistrement. |
| watermarkText | java.lang.String | Texte affiché comme filigrane. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Définit des options supplémentaires pour le filigrane texte. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes)
```


Ajoute un filigrane image dans le document avec des options. Rend la sortie en images.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Les options d'enregistrement. |
| watermarkImageBytes | byte[] | Octets d'image affichés comme filigrane. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes, ImageWatermarkOptions options) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-byte---com.aspose.words.ImageWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, byte[] watermarkImageBytes, ImageWatermarkOptions options)
```


Ajoute un filigrane image dans le document avec des options. Rend la sortie en images.

 **Examples:** 

Montre comment insérer une image de filigrane dans le document et enregistrer le résultat en images.

```

 String doc = getMyDir() + "Document.docx";
 String watermarkImage = getImageDir() + "Logo.jpg";
 Path watermarkImagePath = Paths.get(watermarkImage);

 Watermarker.setWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.PNG), Files.readAllBytes(watermarkImagePath));

 ImageWatermarkOptions options = new ImageWatermarkOptions();
 options.setScale(50.0);
 Watermarker.setWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.PNG), Files.readAllBytes(watermarkImagePath), options);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Les options d'enregistrement. |
| watermarkImageBytes | byte[] | Octets d'image affichés comme filigrane. |
| options | [ImageWatermarkOptions](../../com.aspose.words/imagewatermarkoptions/) | Définit des options supplémentaires pour le filigrane image. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText)
```


Ajoute un filigrane texte dans le document avec des options. Rend la sortie en images.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Les options d'enregistrement. |
| watermarkText | java.lang.String | Texte affiché comme filigrane. |

**Returns:**
java.io.OutputStream[]
### setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options) {#setWatermarkToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-com.aspose.words.TextWatermarkOptions}
```
public static OutputStream[] setWatermarkToImages(String inputFileName, ImageSaveOptions saveOptions, String watermarkText, TextWatermarkOptions options)
```


Ajoute un filigrane texte dans le document avec des options. Rend la sortie en images.

 **Examples:** 

Montre comment insérer du texte de filigrane dans le document et enregistrer le résultat en images.

```

 String doc = getMyDir() + "Big document.docx";
 String watermarkText = "This is a watermark";

 OutputStream[] images = Watermarker.setWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.PNG), watermarkText);

 TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
 watermarkOptions.setColor(Color.RED);
 images = Watermarker.setWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.PNG), watermarkText, watermarkOptions);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | java.lang.String | Le nom de fichier d'entrée. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Les options d'enregistrement. |
| watermarkText | java.lang.String | Texte affiché comme filigrane. |
| options | [TextWatermarkOptions](../../com.aspose.words/textwatermarkoptions/) | Définit des options supplémentaires pour le filigrane texte. |

**Returns:**
java.io.OutputStream[]
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


Spécifie le fichier de sortie pour le processeur.

 **Remarks:** 

Si la sortie se compose de plusieurs fichiers, le nom de fichier de sortie spécifié est utilisé pour générer le nom de fichier de chaque partie selon la règle : 'outputFile\_partIndex.extension'.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.lang.String | Nom du fichier de sortie. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


Spécifie le fichier de sortie pour le processeur.

 **Remarks:** 

Si la sortie se compose de plusieurs fichiers, le nom de fichier de sortie spécifié est utilisé pour générer le nom de fichier de chaque partie selon la règle : 'outputFile\_partIndex.extension'.

 **Examples:** 

Montre comment fusionner des documents en un seul document de sortie en utilisant le contexte.

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

Montre comment convertir des documents avec une seule ligne de code en utilisant le contexte.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.lang.String | Nom du fichier de sortie. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Options d'enregistrement facultatives. Si non spécifiées, le format d'enregistrement est déterminé par l'extension du fichier. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sortie | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
