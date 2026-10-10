---
title: "Reemplazador"
linktitle: "Reemplazador"
second_title: "Aspose.Words para Java"
description: "Proporciona métodos destinados a buscar y reemplazar texto en el documento en Java."
type: docs
weight: 567
url: /es/java/com.aspose.words/replacer/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.Processor](../../com.aspose.words/processor/)
```
public class Replacer extends Processor
```

Proporciona métodos destinados a buscar y reemplazar texto en el documento.
## Métodos

| Método | Descripción |
| --- | --- |
| [create(ReplacerContext context)](#create-com.aspose.words.ReplacerContext) | Crea una nueva instancia del procesador de reemplazo. |
| [execute()](#execute) | Ejecuta la acción del procesador. |
| [from(InputStream input)](#from-java.io.InputStream) | Especifica el documento de entrada para el procesamiento. |
| [from(InputStream input, LoadOptions loadOptions)](#from-java.io.InputStream-com.aspose.words.LoadOptions) | Especifica el documento de entrada para el procesamiento. |
| [from(String input)](#from-java.lang.String) | Especifica el documento de entrada para el procesamiento. |
| [from(String input, LoadOptions loadOptions)](#from-java.lang.String-com.aspose.words.LoadOptions) | Especifica el documento de entrada para el procesamiento. |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement)](#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String) |  |
| [replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String) | Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada, con el formato de guardado especificado y opciones adicionales. |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) | Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada, con el formato de guardado especificado y opciones adicionales. |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String) | Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada usando una expresión regular, con el formato de guardado especificado y opciones adicionales. |
| [replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) | Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada usando una expresión regular, con el formato de guardado especificado y opciones adicionales. |
| [replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement)](#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String) |  |
| [replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement)](#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String) |  |
| [replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) |  |
| [replace(String inputFileName, String outputFileName, String pattern, String replacement)](#replace-java.lang.String-java.lang.String-java.lang.String-java.lang.String) | Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada. |
| [replace(String inputFileName, String outputFileName, Pattern pattern, String replacement)](#replace-java.lang.String-java.lang.String-java.util.regex.Pattern-java.lang.String) | Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada usando una expresión regular. |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String) | Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada. |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) | Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada. |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String) | Reemplaza todas las apariciones de un patrón de expresión regular especificado con una cadena de reemplazo en el archivo de entrada. |
| [replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) | Reemplaza todas las apariciones de un patrón de expresión regular especificado con una cadena de reemplazo en el archivo de entrada. |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String) | Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada. |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions) | Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada. |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String) | Reemplaza todas las apariciones de un patrón de expresión regular especificado con una cadena de reemplazo en el archivo de entrada. |
| [replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)](#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions) | Reemplaza todas las apariciones de un patrón de expresión regular especificado con una cadena de reemplazo en el archivo de entrada. |
| [to(OutputStream output, SaveOptions saveOptions)](#to-java.io.OutputStream-com.aspose.words.SaveOptions) |  |
| [to(OutputStream output, int saveFormat)](#to-java.io.OutputStream-int) |  |
| [to(String output)](#to-java.lang.String) | Especifica el archivo de salida para el procesador. |
| [to(String output, SaveOptions saveOptions)](#to-java.lang.String-com.aspose.words.SaveOptions) | Especifica el archivo de salida para el procesador. |
| [to(String output, int saveFormat)](#to-java.lang.String-int) |  |
| [to(ArrayList output, SaveOptions saveOptions)](#to-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [to(ArrayList output, int saveFormat)](#to-java.util.ArrayList-int) |  |
| [toOutput(ArrayList output, SaveOptions saveOptions)](#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions) |  |
| [toOutput(ArrayList output, int saveFormat)](#toOutput-java.util.ArrayList-int) |  |
### create(ReplacerContext context) {#create-com.aspose.words.ReplacerContext}
```
public static Replacer create(ReplacerContext context)
```


Crea una nueva instancia del procesador de reemplazo.

 **Examples:** 

Muestra cómo reemplazar una cadena en el documento usando contexto.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContext.docx")
         .execute();
 
```

Muestra cómo reemplazar una cadena en el documento usando documentos del flujo usando contexto.

```

 // There is a several ways to replace string in the document using documents from the stream:
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Footer.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStream.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

Muestra cómo reemplazar una cadena con expresiones regulares en el documento usando contexto.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 ReplacerContext replacerContext = new ReplacerContext();
 replacerContext.setReplacement(pattern, replacement);
 replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

 Replacer.create(replacerContext)
         .from(doc)
         .to(getArtifactsDir() + "LowCode.ReplaceContextRegex.docx")
         .execute();
 
```

Muestra cómo reemplazar una cadena con expresiones regulares en el documento usando documentos del flujo usando contexto.

```

 // There is a several ways to replace string with regex in the document using documents from the stream:
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Replace regex.docx")) {
     ReplacerContext replacerContext = new ReplacerContext();
     replacerContext.setReplacement(pattern, replacement);
     replacerContext.getFindReplaceOptions().setFindWholeWordsOnly(false);

     try (FileOutputStream streamOut = new FileOutputStream(getArtifactsDir() + "LowCode.ReplaceContextStreamRegex.docx")) {
         Replacer.create(replacerContext)
                 .from(streamIn)
                 .to(streamOut, SaveFormat.DOCX)
                 .execute();
     }
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| context | [ReplacerContext](../../com.aspose.words/replacercontext/) |  |

**Returns:**
[Replacer](../../com.aspose.words/replacer/)
### execute() {#execute}
```
public void execute()
```


Ejecuta la acción del procesador.

 **Examples:** 

Muestra cómo combinar documentos en un único documento de salida usando el contexto.

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

Muestra cómo combinar documentos del flujo en un único documento de salida usando el contexto.

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

Muestra cómo convertir documentos con una sola línea de código usando el contexto.

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

Muestra cómo convertir documentos del flujo con una sola línea de código usando el contexto.

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


Especifica el documento de entrada para el procesamiento.

 **Remarks:** 

Si el procesador acepta solo un archivo como entrada, solo se procesará el último archivo especificado. El procesador [Merger](../../com.aspose.words/merger/) acepta varios archivos como entrada, como resultado todos los documentos especificados se combinarán. El procesador [Converter](../../com.aspose.words/converter/) acepta solo un archivo como entrada, por lo que solo se convertirá el último archivo especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| entrada | java.io.InputStream | Flujo del documento de entrada. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(InputStream input, LoadOptions loadOptions) {#from-java.io.InputStream-com.aspose.words.LoadOptions}
```
public Processor from(InputStream input, LoadOptions loadOptions)
```


Especifica el documento de entrada para el procesamiento.

 **Remarks:** 

Si el procesador acepta solo un archivo como entrada, solo se procesará el último archivo especificado. El procesador [Merger](../../com.aspose.words/merger/) acepta varios archivos como entrada, como resultado todos los documentos especificados se combinarán. El procesador [Converter](../../com.aspose.words/converter/) acepta solo un archivo como entrada, por lo que solo se convertirá el último archivo especificado.

 **Examples:** 

Muestra cómo combinar documentos del flujo en un único documento de salida usando el contexto.

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

Muestra cómo convertir documentos del flujo con una sola línea de código usando el contexto.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| entrada | java.io.InputStream | Flujo del documento de entrada. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Opciones de carga opcionales usadas para cargar el documento. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file stream.
### from(String input) {#from-java.lang.String}
```
public Processor from(String input)
```


Especifica el documento de entrada para el procesamiento.

 **Remarks:** 

Si el procesador acepta solo un archivo como entrada, solo se procesará el último archivo especificado. El procesador [Merger](../../com.aspose.words/merger/) acepta varios archivos como entrada, como resultado todos los documentos especificados se combinarán. El procesador [Converter](../../com.aspose.words/converter/) acepta solo un archivo como entrada, por lo que solo se convertirá el último archivo especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| entrada | java.lang.String | Nombre de archivo del documento de entrada. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### from(String input, LoadOptions loadOptions) {#from-java.lang.String-com.aspose.words.LoadOptions}
```
public Processor from(String input, LoadOptions loadOptions)
```


Especifica el documento de entrada para el procesamiento.

 **Remarks:** 

Si el procesador acepta solo un archivo como entrada, solo se procesará el último archivo especificado. El procesador [Merger](../../com.aspose.words/merger/) acepta varios archivos como entrada, como resultado todos los documentos especificados se combinarán. El procesador [Converter](../../com.aspose.words/converter/) acepta solo un archivo como entrada, por lo que solo se convertirá el último archivo especificado.

 **Examples:** 

Muestra cómo combinar documentos en un único documento de salida usando el contexto.

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

Muestra cómo convertir documentos con una sola línea de código usando el contexto.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| entrada | java.lang.String | Nombre de archivo del documento de entrada. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions/) | Opciones de carga opcionales usadas para cargar el documento. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified input file.
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| patrón | java.lang.String |  |
| reemplazo | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| patrón | java.lang.String |  |
| reemplazo | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| patrón | java.util.regex.Pattern |  |
| reemplazo | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |
| patrón | java.util.regex.Pattern |  |
| reemplazo | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| patrón | java.lang.String |  |
| reemplazo | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, String pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| patrón | java.lang.String |  |
| reemplazo | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement) {#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| patrón | java.util.regex.Pattern |  |
| reemplazo | java.lang.String |  |

**Returns:**
int
### replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.io.InputStream-java.io.OutputStream-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(InputStream inputStream, OutputStream outputStream, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream |  |
| outputStream | java.io.OutputStream |  |
| saveFormat | int |  |
| patrón | java.util.regex.Pattern |  |
| reemplazo | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement)
```


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada, con el formato de guardado especificado y opciones adicionales.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Las opciones de guardado. |
| patrón | java.lang.String | Una cadena a ser reemplazada. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |

**Returns:**
int - El número de reemplazos realizados.
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada, con el formato de guardado especificado y opciones adicionales.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Las opciones de guardado. |
| patrón | java.lang.String | Una cadena a ser reemplazada. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) objeto para especificar opciones adicionales. |

**Returns:**
int - El número de reemplazos realizados.
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement)
```


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada usando una expresión regular, con el formato de guardado especificado y opciones adicionales.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Las opciones de guardado. |
| patrón | java.util.regex.Pattern | Un patrón de expresión regular usado para encontrar coincidencias. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |

**Returns:**
int - El número de reemplazos realizados.
### replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-com.aspose.words.SaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, SaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada usando una expresión regular, con el formato de guardado especificado y opciones adicionales.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Las opciones de guardado. |
| patrón | java.util.regex.Pattern | Un patrón de expresión regular usado para encontrar coincidencias. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) objeto para especificar opciones adicionales. |

**Returns:**
int - El número de reemplazos realizados.
### replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement) {#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| patrón | java.lang.String |  |
| reemplazo | java.lang.String |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-int-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, String pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| patrón | java.lang.String |  |
| reemplazo | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement) {#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| patrón | java.util.regex.Pattern |  |
| reemplazo | java.lang.String |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-int-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static int replace(String inputFileName, String outputFileName, int saveFormat, Pattern pattern, String replacement, FindReplaceOptions options)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String |  |
| outputFileName | java.lang.String |  |
| saveFormat | int |  |
| patrón | java.util.regex.Pattern |  |
| reemplazo | java.lang.String |  |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) |  |

**Returns:**
int
### replace(String inputFileName, String outputFileName, String pattern, String replacement) {#replace-java.lang.String-java.lang.String-java.lang.String-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, String pattern, String replacement)
```


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

 **Examples:** 

Muestra cómo reemplazar una cadena en el documento.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 FindReplaceOptions options = new FindReplaceOptions();
 options.setFindWholeWordsOnly(false);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.Replace.1.docx", pattern, replacement);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.Replace.2.docx", SaveFormat.DOCX, pattern, replacement);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.Replace.3.docx", SaveFormat.DOCX, pattern, replacement, options);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| patrón | java.lang.String | Una cadena a ser reemplazada. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |

**Returns:**
int - El número de reemplazos realizados.
### replace(String inputFileName, String outputFileName, Pattern pattern, String replacement) {#replace-java.lang.String-java.lang.String-java.util.regex.Pattern-java.lang.String}
```
public static int replace(String inputFileName, String outputFileName, Pattern pattern, String replacement)
```


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada usando una expresión regular.

 **Remarks:** 

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar nombres de archivo para cada parte siguiendo la regla: outputFile\_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

 **Examples:** 

Muestra cómo reemplazar una cadena con expresiones regulares en el documento.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "gr(a|e)y";
 String replacement = "lavender";

 Replacer.replace(doc, getArtifactsDir() + "LowCode.ReplaceRegex.1.docx", pattern, replacement);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.ReplaceRegex.2.docx", SaveFormat.DOCX, pattern, replacement);
 FindReplaceOptions options = new FindReplaceOptions();
 options.setFindWholeWordsOnly(false);
 Replacer.replace(doc, getArtifactsDir() + "LowCode.ReplaceRegex.3.docx", SaveFormat.DOCX, pattern, replacement, options);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| outputFileName | java.lang.String | El nombre del archivo de salida. |
| patrón | java.util.regex.Pattern | Un patrón de expresión regular usado para encontrar coincidencias. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |

**Returns:**
int - El número de reemplazos realizados.
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement)
```


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada. Renderiza la salida a imágenes.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream | El flujo de archivo de entrada. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Las opciones de guardado. |
| patrón | java.lang.String | Una cadena a ser reemplazada. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada. Renderiza la salida a imágenes.

 **Examples:** 

Muestra cómo reemplazar una cadena en el documento usando documentos del flujo y guardar el resultado en imágenes.

```

 // There is a several ways to replace string in the document using documents from the stream:
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Footer.docx")) {
     OutputStream[] images = Replacer.replaceToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement);

     FindReplaceOptions options = new FindReplaceOptions();
     options.setFindWholeWordsOnly(false);
     images = Replacer.replaceToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement, options);
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream | El flujo de archivo de entrada. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Las opciones de guardado. |
| patrón | java.lang.String | Una cadena a ser reemplazada. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) objeto para especificar opciones adicionales. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement)
```


Reemplaza todas las apariciones de un patrón de expresión regular especificado con una cadena de reemplazo en el archivo de entrada. Renderiza la salida a imágenes.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream | El flujo de archivo de entrada. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Las opciones de guardado. |
| patrón | java.util.regex.Pattern | Un patrón de expresión regular usado para encontrar coincidencias. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.io.InputStream-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(InputStream inputStream, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```


Reemplaza todas las apariciones de un patrón de expresión regular especificado con una cadena de reemplazo en el archivo de entrada. Renderiza la salida a imágenes.

 **Examples:** 

Muestra cómo reemplazar una cadena con expresiones regulares en el documento usando documentos del flujo y guardar el resultado en imágenes.

```

 // There is a several ways to replace string with regex in the document using documents from the stream:
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 try (FileInputStream streamIn = new FileInputStream(getMyDir() + "Replace regex.docx")) {
     OutputStream[] images = Replacer.replaceToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement);
     FindReplaceOptions options = new FindReplaceOptions();
     options.setFindWholeWordsOnly(false);
     images = Replacer.replaceToImages(streamIn, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement, options);
 }
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | java.io.InputStream | El flujo de archivo de entrada. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Las opciones de guardado. |
| patrón | java.util.regex.Pattern | Un patrón de expresión regular usado para encontrar coincidencias. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) objeto para especificar opciones adicionales. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement)
```


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada. Renderiza la salida a imágenes.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Las opciones de guardado. |
| patrón | java.lang.String | Una cadena a ser reemplazada. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, String pattern, String replacement, FindReplaceOptions options)
```


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada. Renderiza la salida a imágenes.

 **Examples:** 

Muestra cómo reemplazar una cadena en el documento y guardar el resultado en imágenes.

```

 // There is a several ways to replace string in the document:
 String doc = getMyDir() + "Footer.docx";
 String pattern = "(C)2006 Aspose Pty Ltd.";
 String replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

 OutputStream[] images = Replacer.replaceToImages(doc, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement);

 FindReplaceOptions options = new FindReplaceOptions();
 options.setFindWholeWordsOnly(false);
 images = Replacer.replaceToImages(doc, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement, options);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Las opciones de guardado. |
| patrón | java.lang.String | Una cadena a ser reemplazada. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) objeto para especificar opciones adicionales. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement)
```


Reemplaza todas las apariciones de un patrón de expresión regular especificado con una cadena de reemplazo en el archivo de entrada. Renderiza la salida a imágenes.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Las opciones de guardado. |
| patrón | java.util.regex.Pattern | Un patrón de expresión regular usado para encontrar coincidencias. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |

**Returns:**
java.io.OutputStream[]
### replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options) {#replaceToImages-java.lang.String-com.aspose.words.ImageSaveOptions-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions}
```
public static OutputStream[] replaceToImages(String inputFileName, ImageSaveOptions saveOptions, Pattern pattern, String replacement, FindReplaceOptions options)
```


Reemplaza todas las apariciones de un patrón de expresión regular especificado con una cadena de reemplazo en el archivo de entrada. Renderiza la salida a imágenes.

 **Examples:** 

Muestra cómo reemplazar una cadena con expresiones regulares en el documento y guardar el resultado en imágenes.

```

 // There is a several ways to replace string with regex in the document:
 String doc = getMyDir() + "Footer.docx";
 Pattern pattern = Pattern.compile("gr(a|e)y");
 String replacement = "lavender";

 OutputStream[] images = Replacer.replaceToImages(doc, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement);
 FindReplaceOptions options = new FindReplaceOptions();
 options.setFindWholeWordsOnly(false);
 images = Replacer.replaceToImages(doc, new ImageSaveOptions(SaveFormat.PNG), pattern, replacement, options);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | java.lang.String | El nombre del archivo de entrada. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Las opciones de guardado. |
| patrón | java.util.regex.Pattern | Un patrón de expresión regular usado para encontrar coincidencias. |
| reemplazo | java.lang.String | Una cadena para reemplazar todas las apariciones del patrón. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions/) objeto para especificar opciones adicionales. |

**Returns:**
java.io.OutputStream[]
### to(OutputStream output, SaveOptions saveOptions) {#to-java.io.OutputStream-com.aspose.words.SaveOptions}
```
public Processor to(OutputStream output, SaveOptions saveOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.io.OutputStream |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(OutputStream output, int saveFormat) {#to-java.io.OutputStream-int}
```
public Processor to(OutputStream output, int saveFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.io.OutputStream |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(String output) {#to-java.lang.String}
```
public Processor to(String output)
```


Especifica el archivo de salida para el procesador.

 **Remarks:** 

Si la salida consiste en varios archivos, el nombre de archivo de salida especificado se usa para generar el nombre de archivo de cada parte siguiendo la regla: 'outputFile\_partIndex.extension'.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.lang.String | Nombre del archivo de salida. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, SaveOptions saveOptions) {#to-java.lang.String-com.aspose.words.SaveOptions}
```
public Processor to(String output, SaveOptions saveOptions)
```


Especifica el archivo de salida para el procesador.

 **Remarks:** 

Si la salida consiste en varios archivos, el nombre de archivo de salida especificado se usa para generar el nombre de archivo de cada parte siguiendo la regla: 'outputFile\_partIndex.extension'.

 **Examples:** 

Muestra cómo combinar documentos en un único documento de salida usando el contexto.

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

Muestra cómo convertir documentos con una sola línea de código usando el contexto.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.lang.String | Nombre del archivo de salida. |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) | Opciones de guardado opcionales. Si no se especifican, el formato de guardado se determina por la extensión del archivo. |

**Returns:**
[Processor](../../com.aspose.words/processor/) - Returns processor with specified output file.
### to(String output, int saveFormat) {#to-java.lang.String-int}
```
public Processor to(String output, int saveFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.lang.String |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, SaveOptions saveOptions) {#to-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor to(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### to(ArrayList output, int saveFormat) {#to-java.util.ArrayList-int}
```
public Processor to(ArrayList output, int saveFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, SaveOptions saveOptions) {#toOutput-java.util.ArrayList-com.aspose.words.SaveOptions}
```
public Processor toOutput(ArrayList output, SaveOptions saveOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.util.ArrayList |  |
| saveOptions | [SaveOptions](../../com.aspose.words/saveoptions/) |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
### toOutput(ArrayList output, int saveFormat) {#toOutput-java.util.ArrayList-int}
```
public Processor toOutput(ArrayList output, int saveFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| salida | java.util.ArrayList |  |
| saveFormat | int |  |

**Returns:**
[Processor](../../com.aspose.words/processor/)
