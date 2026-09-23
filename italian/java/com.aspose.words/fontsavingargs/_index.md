---
title: "FontSavingArgs"
linktitle: "FontSavingArgs"
second_title: "Aspose.Words per Java"
description: "Fornisce dati per l'evento IFontSavingCallback.fontSavingcom.aspose.words.FontSavingArgs in Java."
type: docs
weight: 331
url: /it/java/com.aspose.words/fontsavingargs/
---

**Inheritance:**
java.lang.Object
```
public class FontSavingArgs
```

Fornisce dati per l'evento [IFontSavingCallback.fontSaving(com.aspose.words.FontSavingArgs)](../../com.aspose.words/ifontsavingcallback/\#fontSaving-com.aspose.words.FontSavingArgs).

Per saperne di più, visita l'articolo di documentazione [ Save a Document ][Save a Document].

 **Remarks:** 

Quando Aspose.Words salva un documento in HTML o formati correlati e [HtmlSaveOptions.getExportFontResources()](../../com.aspose.words/htmlsaveoptions/\#getExportFontResources) / [HtmlSaveOptions.setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportFontResources-boolean) è impostato su true, salva ogni font soggetto all'esportazione in un file separato.

[FontSavingArgs](../../com.aspose.words/fontsavingargs/) controls whether particular font resource should be exported and how.

[FontSavingArgs](../../com.aspose.words/fontsavingargs/) also allows to redefine how font file names are generated or to completely circumvent saving of fonts into files by providing your own stream objects.

Per decidere se salvare una risorsa font specifica, usa la proprietà [isExportNeeded()](../../com.aspose.words/fontsavingargs/\#isExportNeeded) / [isExportNeeded(boolean)](../../com.aspose.words/fontsavingargs/\#isExportNeeded-boolean).

Per salvare i font in stream invece di file, usa la proprietà **P:Aspose.Words.Saving.FontSavingArgs.FontStream**.

 **Examples:** 

Mostra come definire una logica personalizzata per l'esportazione dei font durante il salvataggio in HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getBold()](#getBold) | Indica se il font corrente è in grassetto. |
| [getDocument()](#getDocument) | Ottiene l'oggetto documento che viene salvato. |
| [getFontFamilyName()](#getFontFamilyName) | Indica il nome della famiglia del font corrente. |
| [getFontFileName()](#getFontFileName) | Ottiene il nome del file (senza percorso) in cui il font verrà salvato. |
| [getFontStream()](#getFontStream) |  |
| [getItalic()](#getItalic) | Indica se il font corrente è in corsivo. |
| [getKeepFontStreamOpen()](#getKeepFontStreamOpen) | Specifica se Aspose.Words deve mantenere lo stream aperto o chiuderlo dopo aver salvato un font. |
| [getOriginalFileName()](#getOriginalFileName) | Ottiene il nome originale del file font con estensione. |
| [getOriginalFileSize()](#getOriginalFileSize) | Ottiene la dimensione originale del file font. |
| [isExportNeeded()](#isExportNeeded) | Consente di specificare se il font corrente sarà esportato come risorsa font. |
| [isExportNeeded(boolean value)](#isExportNeeded-boolean) | Consente di specificare se il font corrente sarà esportato come risorsa font. |
| [isSubsettingNeeded()](#isSubsettingNeeded) | Consente di specificare se il font corrente sarà sottoposto a subset prima di essere esportato come risorsa font. |
| [isSubsettingNeeded(boolean value)](#isSubsettingNeeded-boolean) | Consente di specificare se il font corrente sarà sottoposto a subset prima di essere esportato come risorsa font. |
| [setFontFileName(String value)](#setFontFileName-java.lang.String) | Imposta il nome del file (senza percorso) in cui il font verrà salvato. |
| [setFontStream(OutputStream value)](#setFontStream-java.io.OutputStream) |  |
| [setKeepFontStreamOpen(boolean value)](#setKeepFontStreamOpen-boolean) | Specifica se Aspose.Words deve mantenere lo stream aperto o chiuderlo dopo aver salvato un font. |
### getBold() {#getBold}
```
public boolean getBold()
```


Indica se il font corrente è in grassetto.

 **Examples:** 

Mostra come definire una logica personalizzata per l'esportazione dei font durante il salvataggio in HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getDocument() {#getDocument}
```
public Document getDocument()
```


Ottiene l'oggetto documento che viene salvato.

 **Examples:** 

Mostra come definire una logica personalizzata per l'esportazione dei font durante il salvataggio in HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**Returns:**
[Document](../../com.aspose.words/document/) - The document object that is being saved.
### getFontFamilyName() {#getFontFamilyName}
```
public String getFontFamilyName()
```


Indica il nome della famiglia del font corrente.

 **Examples:** 

Mostra come definire una logica personalizzata per l'esportazione dei font durante il salvataggio in HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### getFontFileName() {#getFontFileName}
```
public String getFontFileName()
```


Ottiene il nome del file (senza percorso) in cui il font verrà salvato.

 **Remarks:** 

Questa proprietà consente di ridefinire come vengono generati i nomi dei file font durante l'esportazione in HTML.

Quando l'evento viene attivato, questa proprietà contiene il nome file generato da Aspose.Words. È possibile modificare il valore di questa proprietà per salvare il carattere in un file diverso. Nota che i nomi file devono essere univoci.

Aspose.Words genera automaticamente un nome file univoco per ogni carattere incorporato durante l'esportazione in formato HTML. Il modo in cui il nome file del carattere viene generato dipende dal fatto che si salvi il documento su un file o su uno stream.

Quando si salva un documento su un file, il nome file del carattere generato appare come *..*.

Quando si salva un documento su uno stream, il nome file del carattere generato appare come *Aspose.Words...*.

[getFontFileName()](../../com.aspose.words/fontsavingargs/\#getFontFileName) / [setFontFileName(java.lang.String)](../../com.aspose.words/fontsavingargs/\#setFontFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [HtmlSaveOptions.getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [HtmlSaveOptions.setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) and [HtmlSaveOptions.getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [HtmlSaveOptions.setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) properties.

 **Examples:** 

Mostra come definire una logica personalizzata per l'esportazione dei font durante il salvataggio in HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**Returns:**
java.lang.String - Il nome file (senza percorso) dove il carattere verrà salvato.
### getFontStream() {#getFontStream}
```
public OutputStream getFontStream()
```




**Returns:**
java.io.OutputStream
### getItalic() {#getItalic}
```
public boolean getItalic()
```


Indica se il font corrente è in corsivo.

 **Examples:** 

Mostra come definire una logica personalizzata per l'esportazione dei font durante il salvataggio in HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### getKeepFontStreamOpen() {#getKeepFontStreamOpen}
```
public boolean getKeepFontStreamOpen()
```


Specifica se Aspose.Words deve mantenere lo stream aperto o chiuderlo dopo aver salvato un font.

 **Remarks:** 

Il valore predefinito è  false  e Aspose.Words chiuderà lo stream fornito nella proprietà **P:Aspose.Words.Saving.FontSavingArgs.FontStream** dopo aver scritto un carattere al suo interno. Specificare  true  per mantenere lo stream aperto.

 **Examples:** 

Mostra come definire una logica personalizzata per l'esportazione dei font durante il salvataggio in HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**Returns:**
boolean - Il valore booleano corrispondente.
### getOriginalFileName() {#getOriginalFileName}
```
public String getOriginalFileName()
```


Ottiene il nome originale del file font con estensione.

 **Remarks:** 

Questa proprietà contiene il nome file originale del carattere corrente, se noto. Altrimenti può essere una stringa vuota.

 **Examples:** 

Mostra come definire una logica personalizzata per l'esportazione dei font durante il salvataggio in HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**Returns:**
java.lang.String - Il nome file originale del carattere con estensione.
### getOriginalFileSize() {#getOriginalFileSize}
```
public int getOriginalFileSize()
```


Ottiene la dimensione originale del file font.

 **Remarks:** 

Questa proprietà contiene la dimensione file originale del carattere corrente, se nota. Altrimenti può essere zero.

 **Examples:** 

Mostra come definire una logica personalizzata per l'esportazione dei font durante il salvataggio in HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**Returns:**
int - La dimensione file originale del carattere.
### isExportNeeded() {#isExportNeeded}
```
public boolean isExportNeeded()
```


Consente di specificare se il carattere corrente sarà esportato come risorsa di carattere. Il valore predefinito è  true .

 **Examples:** 

Mostra come definire una logica personalizzata per l'esportazione dei font durante il salvataggio in HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### isExportNeeded(boolean value) {#isExportNeeded-boolean}
```
public void isExportNeeded(boolean value)
```


Consente di specificare se il carattere corrente sarà esportato come risorsa di carattere. Il valore predefinito è  true .

 **Examples:** 

Mostra come definire una logica personalizzata per l'esportazione dei font durante il salvataggio in HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### isSubsettingNeeded() {#isSubsettingNeeded}
```
public boolean isSubsettingNeeded()
```


Consente di specificare se il font corrente sarà sottoposto a subset prima di essere esportato come risorsa font.

 **Remarks:** 

I caratteri possono essere esportati come file di carattere originali completi o ridotti per includere solo i caratteri utilizzati nel documento. La riduzione consente di diminuire la dimensione della risorsa di carattere risultante.

Per impostazione predefinita, Aspose.Words decide se eseguire la riduzione confrontando la dimensione originale del file del carattere con quella specificata in [HtmlSaveOptions.getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions/\#getFontResourcesSubsettingSizeThreshold) / [HtmlSaveOptions.setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions/\#setFontResourcesSubsettingSizeThreshold-int). È possibile sovrascrivere questo comportamento per singoli caratteri impostando la proprietà [isSubsettingNeeded()](../../com.aspose.words/fontsavingargs/\#isSubsettingNeeded) / [isSubsettingNeeded(boolean)](../../com.aspose.words/fontsavingargs/\#isSubsettingNeeded-boolean).

 **Examples:** 

Mostra come definire una logica personalizzata per l'esportazione dei font durante il salvataggio in HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**Returns:**
boolean - Il valore booleano corrispondente.
### isSubsettingNeeded(boolean value) {#isSubsettingNeeded-boolean}
```
public void isSubsettingNeeded(boolean value)
```


Consente di specificare se il font corrente sarà sottoposto a subset prima di essere esportato come risorsa font.

 **Remarks:** 

I caratteri possono essere esportati come file di carattere originali completi o ridotti per includere solo i caratteri utilizzati nel documento. La riduzione consente di diminuire la dimensione della risorsa di carattere risultante.

Per impostazione predefinita, Aspose.Words decide se eseguire la riduzione confrontando la dimensione originale del file del carattere con quella specificata in [HtmlSaveOptions.getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions/\#getFontResourcesSubsettingSizeThreshold) / [HtmlSaveOptions.setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions/\#setFontResourcesSubsettingSizeThreshold-int). È possibile sovrascrivere questo comportamento per singoli caratteri impostando la proprietà [isSubsettingNeeded()](../../com.aspose.words/fontsavingargs/\#isSubsettingNeeded) / [isSubsettingNeeded(boolean)](../../com.aspose.words/fontsavingargs/\#isSubsettingNeeded-boolean).

 **Examples:** 

Mostra come definire una logica personalizzata per l'esportazione dei font durante il salvataggio in HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setFontFileName(String value) {#setFontFileName-java.lang.String}
```
public void setFontFileName(String value)
```


Imposta il nome del file (senza percorso) in cui il font verrà salvato.

 **Remarks:** 

Questa proprietà consente di ridefinire come vengono generati i nomi dei file font durante l'esportazione in HTML.

Quando l'evento viene attivato, questa proprietà contiene il nome file generato da Aspose.Words. È possibile modificare il valore di questa proprietà per salvare il carattere in un file diverso. Nota che i nomi file devono essere univoci.

Aspose.Words genera automaticamente un nome file univoco per ogni carattere incorporato durante l'esportazione in formato HTML. Il modo in cui il nome file del carattere viene generato dipende dal fatto che si salvi il documento su un file o su uno stream.

Quando si salva un documento su un file, il nome file del carattere generato appare come *..*.

Quando si salva un documento su uno stream, il nome file del carattere generato appare come *Aspose.Words...*.

[getFontFileName()](../../com.aspose.words/fontsavingargs/\#getFontFileName) / [setFontFileName(java.lang.String)](../../com.aspose.words/fontsavingargs/\#setFontFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [HtmlSaveOptions.getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [HtmlSaveOptions.setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) and [HtmlSaveOptions.getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [HtmlSaveOptions.setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) properties.

 **Examples:** 

Mostra come definire una logica personalizzata per l'esportazione dei font durante il salvataggio in HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il nome file (senza percorso) dove il carattere sarà salvato. |

### setFontStream(OutputStream value) {#setFontStream-java.io.OutputStream}
```
public void setFontStream(OutputStream value)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.io.OutputStream |  |

### setKeepFontStreamOpen(boolean value) {#setKeepFontStreamOpen-boolean}
```
public void setKeepFontStreamOpen(boolean value)
```


Specifica se Aspose.Words deve mantenere lo stream aperto o chiuderlo dopo aver salvato un font.

 **Remarks:** 

Il valore predefinito è  false  e Aspose.Words chiuderà lo stream fornito nella proprietà **P:Aspose.Words.Saving.FontSavingArgs.FontStream** dopo aver scritto un carattere al suo interno. Specificare  true  per mantenere lo stream aperto.

 **Examples:** 

Mostra come definire una logica personalizzata per l'esportazione dei font durante il salvataggio in HTML.

```

 public void saveExportedFonts() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     // Configure a SaveOptions object to export fonts to separate files.
     // Set a callback that will handle font saving in a custom manner.
     HtmlSaveOptions options = new HtmlSaveOptions();
     {
         options.setExportFontResources(true);
         options.setFontSavingCallback(new HandleFontSaving());
     }

     // The callback will export .ttf files and save them alongside the output document.
     doc.save(getArtifactsDir() + "HtmlSaveOptions.SaveExportedFonts.html", options);

     File[] fontFileNames = new File(getArtifactsDir()).listFiles((d, name) -> name.endsWith(".ttf"));

     for (File fontFilename : fontFileNames) {
         System.out.println(fontFilename.getName());
     }

 }

 /// 
 /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
 /// 
 public static class HandleFontSaving implements IFontSavingCallback {
     public void fontSaving(FontSavingArgs args) throws Exception {
         System.out.println(MessageFormat.format("Font:\t{0}", args.getFontFamilyName()));
         if (args.getBold()) System.out.print(", bold");
         if (args.getItalic()) System.out.print(", italic");
         System.out.println(MessageFormat.format("\nSource:\t{0}, {1} bytes\n", args.getOriginalFileName(), args.getOriginalFileSize()));

         // We can also access the source document from here.
         Assert.assertTrue(args.getDocument().getOriginalFileName().endsWith("Rendering.docx"));

         Assert.assertTrue(args.isExportNeeded());
         Assert.assertTrue(args.isSubsettingNeeded());

         String[] splittedFileName = args.getOriginalFileName().split("\\\\");
         String fileName = splittedFileName[splittedFileName.length - 1];

         // There are two ways of saving an exported font.
         // 1 -  Save it to a local file system location:
         args.setFontFileName(fileName);

         // 2 -  Save it to a stream:
         args.setFontStream(new FileOutputStream(fileName));
         Assert.assertFalse(args.getKeepFontStreamOpen());
     }
 }
 
```

**P:Aspose.Words.Saving.FontSavingArgs.FontStream**

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

