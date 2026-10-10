---
title: "FontSavingArgs"
linktitle: "FontSavingArgs"
second_title: "Aspose.Words für Java"
description: "Stellt Daten für das Ereignis IFontSavingCallback.fontSavingcom.aspose.words.FontSavingArgs in Java bereit."
type: docs
weight: 331
url: /de/java/com.aspose.words/fontsavingargs/
---

**Inheritance:**
java.lang.Object
```
public class FontSavingArgs
```

Stellt Daten für das [IFontSavingCallback.fontSaving(com.aspose.words.FontSavingArgs)](../../com.aspose.words/ifontsavingcallback/\#fontSaving-com.aspose.words.FontSavingArgs) Ereignis bereit.

Um mehr zu erfahren, besuchen Sie den [ Save a Document ][Save a Document] Dokumentationsartikel.

 **Remarks:** 

Wenn Aspose.Words ein Dokument in HTML oder verwandte Formate speichert und [HtmlSaveOptions.getExportFontResources()](../../com.aspose.words/htmlsaveoptions/\#getExportFontResources) / [HtmlSaveOptions.setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions/\#setExportFontResources-boolean) auf  true  gesetzt ist, speichert es jede Schriftart, die exportiert werden soll, in einer separaten Datei.

[FontSavingArgs](../../com.aspose.words/fontsavingargs/) controls whether particular font resource should be exported and how.

[FontSavingArgs](../../com.aspose.words/fontsavingargs/) also allows to redefine how font file names are generated or to completely circumvent saving of fonts into files by providing your own stream objects.

Um zu entscheiden, ob eine bestimmte Schriftressource gespeichert werden soll, verwenden Sie die [isExportNeeded()](../../com.aspose.words/fontsavingargs/\#isExportNeeded) / [isExportNeeded(boolean)](../../com.aspose.words/fontsavingargs/\#isExportNeeded-boolean) Eigenschaft.

Um Schriftarten in Streams statt in Dateien zu speichern, verwenden Sie die **P:Aspose.Words.Saving.FontSavingArgs.FontStream**-Eigenschaft.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für das Exportieren von Schriftarten beim Speichern nach HTML definiert wird.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getBold()](#getBold) | Gibt an, ob die aktuelle Schriftart fett ist. |
| [getDocument()](#getDocument) | Ruft das Dokumentobjekt ab, das gespeichert wird. |
| [getFontFamilyName()](#getFontFamilyName) | Gibt den Namen der aktuellen Schriftfamilie an. |
| [getFontFileName()](#getFontFileName) | Ruft den Dateinamen (ohne Pfad) ab, in dem die Schriftart gespeichert wird. |
| [getFontStream()](#getFontStream) |  |
| [getItalic()](#getItalic) | Gibt an, ob die aktuelle Schriftart kursiv ist. |
| [getKeepFontStreamOpen()](#getKeepFontStreamOpen) | Legt fest, ob Aspose.Words den Stream nach dem Speichern einer Schriftart offen lassen oder schließen soll. |
| [getOriginalFileName()](#getOriginalFileName) | Ruft den ursprünglichen Schriftdateinamen mit Erweiterung ab. |
| [getOriginalFileSize()](#getOriginalFileSize) | Ruft die ursprüngliche Schriftdateigröße ab. |
| [isExportNeeded()](#isExportNeeded) | Ermöglicht die Angabe, ob die aktuelle Schriftart als Schriftressource exportiert wird. |
| [isExportNeeded(boolean value)](#isExportNeeded-boolean) | Ermöglicht die Angabe, ob die aktuelle Schriftart als Schriftressource exportiert wird. |
| [isSubsettingNeeded()](#isSubsettingNeeded) | Ermöglicht die Angabe, ob die aktuelle Schriftart vor dem Export als Schriftressource teilunterteilt wird. |
| [isSubsettingNeeded(boolean value)](#isSubsettingNeeded-boolean) | Ermöglicht die Angabe, ob die aktuelle Schriftart vor dem Export als Schriftressource teilunterteilt wird. |
| [setFontFileName(String value)](#setFontFileName-java.lang.String) | Setzt den Dateinamen (ohne Pfad), in dem die Schriftart gespeichert wird. |
| [setFontStream(OutputStream value)](#setFontStream-java.io.OutputStream) |  |
| [setKeepFontStreamOpen(boolean value)](#setKeepFontStreamOpen-boolean) | Legt fest, ob Aspose.Words den Stream nach dem Speichern einer Schriftart offen lassen oder schließen soll. |
### getBold() {#getBold}
```
public boolean getBold()
```


Gibt an, ob die aktuelle Schriftart fett ist.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für das Exportieren von Schriftarten beim Speichern nach HTML definiert wird.

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
boolean - Der entsprechende  boolean  Wert.
### getDocument() {#getDocument}
```
public Document getDocument()
```


Ruft das Dokumentobjekt ab, das gespeichert wird.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für das Exportieren von Schriftarten beim Speichern nach HTML definiert wird.

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


Gibt den Namen der aktuellen Schriftfamilie an.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für das Exportieren von Schriftarten beim Speichern nach HTML definiert wird.

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
java.lang.String - Der entsprechende java.lang.String-Wert.
### getFontFileName() {#getFontFileName}
```
public String getFontFileName()
```


Ruft den Dateinamen (ohne Pfad) ab, in dem die Schriftart gespeichert wird.

 **Remarks:** 

Diese Eigenschaft ermöglicht es Ihnen, die Art und Weise, wie Schriftdateinamen beim Export nach HTML erzeugt werden, neu zu definieren.

Wenn das Ereignis ausgelöst wird, enthält diese Eigenschaft den von Aspose.Words erzeugten Dateinamen. Sie können den Wert dieser Eigenschaft ändern, um die Schriftart in einer anderen Datei zu speichern. Beachten Sie, dass Dateinamen eindeutig sein müssen.

Aspose.Words erzeugt beim Export in das HTML-Format automatisch einen eindeutigen Dateinamen für jede eingebettete Schriftart. Wie der Schriftdateiname erzeugt wird, hängt davon ab, ob Sie das Dokument in einer Datei oder in einem Stream speichern.

Beim Speichern eines Dokuments in einer Datei sieht der erzeugte Schriftdateiname wie *..* aus.

Beim Speichern eines Dokuments in einem Stream sieht der erzeugte Schriftdateiname wie *Aspose.Words...* aus.

[getFontFileName()](../../com.aspose.words/fontsavingargs/\#getFontFileName) / [setFontFileName(java.lang.String)](../../com.aspose.words/fontsavingargs/\#setFontFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [HtmlSaveOptions.getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [HtmlSaveOptions.setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) and [HtmlSaveOptions.getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [HtmlSaveOptions.setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) properties.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für das Exportieren von Schriftarten beim Speichern nach HTML definiert wird.

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
java.lang.String – Der Dateiname (ohne Pfad), in dem die Schriftart gespeichert wird.
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


Gibt an, ob die aktuelle Schriftart kursiv ist.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für das Exportieren von Schriftarten beim Speichern nach HTML definiert wird.

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
boolean - Der entsprechende  boolean  Wert.
### getKeepFontStreamOpen() {#getKeepFontStreamOpen}
```
public boolean getKeepFontStreamOpen()
```


Legt fest, ob Aspose.Words den Stream nach dem Speichern einer Schriftart offen lassen oder schließen soll.

 **Remarks:** 

Standard ist  false  und Aspose.Words schließt den Stream, den Sie in der **P:Aspose.Words.Saving.FontSavingArgs.FontStream**-Eigenschaft angegeben haben, nachdem eine Schriftart darin geschrieben wurde. Geben Sie  true  an, um den Stream offen zu lassen.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für das Exportieren von Schriftarten beim Speichern nach HTML definiert wird.

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
boolean - Der entsprechende  boolean  Wert.
### getOriginalFileName() {#getOriginalFileName}
```
public String getOriginalFileName()
```


Ruft den ursprünglichen Schriftdateinamen mit Erweiterung ab.

 **Remarks:** 

Diese Eigenschaft enthält den ursprünglichen Dateinamen der aktuellen Schriftart, falls bekannt. Andernfalls kann sie eine leere Zeichenkette sein.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für das Exportieren von Schriftarten beim Speichern nach HTML definiert wird.

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
java.lang.String – Der ursprüngliche Schriftdateiname mit Erweiterung.
### getOriginalFileSize() {#getOriginalFileSize}
```
public int getOriginalFileSize()
```


Ruft die ursprüngliche Schriftdateigröße ab.

 **Remarks:** 

Diese Eigenschaft enthält die ursprüngliche Dateigröße der aktuellen Schrift, falls sie bekannt ist. Andernfalls kann sie Null sein.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für das Exportieren von Schriftarten beim Speichern nach HTML definiert wird.

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
int – Die ursprüngliche Schriftdateigröße.
### isExportNeeded() {#isExportNeeded}
```
public boolean isExportNeeded()
```


Ermöglicht die Angabe, ob die aktuelle Schrift als Schriftressource exportiert wird. Standard ist true.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für das Exportieren von Schriftarten beim Speichern nach HTML definiert wird.

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
boolean - Der entsprechende  boolean  Wert.
### isExportNeeded(boolean value) {#isExportNeeded-boolean}
```
public void isExportNeeded(boolean value)
```


Ermöglicht die Angabe, ob die aktuelle Schrift als Schriftressource exportiert wird. Standard ist true.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für das Exportieren von Schriftarten beim Speichern nach HTML definiert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### isSubsettingNeeded() {#isSubsettingNeeded}
```
public boolean isSubsettingNeeded()
```


Ermöglicht die Angabe, ob die aktuelle Schriftart vor dem Export als Schriftressource teilunterteilt wird.

 **Remarks:** 

Schriften können als vollständige Originalschriftdateien exportiert oder auf Teilmengen reduziert werden, um nur die im Dokument verwendeten Zeichen einzuschließen. Das Subsetzen ermöglicht die Reduzierung der resultierenden Schriftressourcengröße.

Standard entscheidet Aspose.Words, ob ein Subsetting durchgeführt wird, indem die ursprüngliche Schriftdateigröße mit der in [HtmlSaveOptions.getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions/\#getFontResourcesSubsettingSizeThreshold) / [HtmlSaveOptions.setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions/\#setFontResourcesSubsettingSizeThreshold-int) angegebenen verglichen wird. Sie können dieses Verhalten für einzelne Schriften überschreiben, indem Sie die Eigenschaft [isSubsettingNeeded()](../../com.aspose.words/fontsavingargs/\#isSubsettingNeeded) / [isSubsettingNeeded(boolean)](../../com.aspose.words/fontsavingargs/\#isSubsettingNeeded-boolean) setzen.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für das Exportieren von Schriftarten beim Speichern nach HTML definiert wird.

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
boolean - Der entsprechende  boolean  Wert.
### isSubsettingNeeded(boolean value) {#isSubsettingNeeded-boolean}
```
public void isSubsettingNeeded(boolean value)
```


Ermöglicht die Angabe, ob die aktuelle Schriftart vor dem Export als Schriftressource teilunterteilt wird.

 **Remarks:** 

Schriften können als vollständige Originalschriftdateien exportiert oder auf Teilmengen reduziert werden, um nur die im Dokument verwendeten Zeichen einzuschließen. Das Subsetzen ermöglicht die Reduzierung der resultierenden Schriftressourcengröße.

Standard entscheidet Aspose.Words, ob ein Subsetting durchgeführt wird, indem die ursprüngliche Schriftdateigröße mit der in [HtmlSaveOptions.getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions/\#getFontResourcesSubsettingSizeThreshold) / [HtmlSaveOptions.setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions/\#setFontResourcesSubsettingSizeThreshold-int) angegebenen verglichen wird. Sie können dieses Verhalten für einzelne Schriften überschreiben, indem Sie die Eigenschaft [isSubsettingNeeded()](../../com.aspose.words/fontsavingargs/\#isSubsettingNeeded) / [isSubsettingNeeded(boolean)](../../com.aspose.words/fontsavingargs/\#isSubsettingNeeded-boolean) setzen.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für das Exportieren von Schriftarten beim Speichern nach HTML definiert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setFontFileName(String value) {#setFontFileName-java.lang.String}
```
public void setFontFileName(String value)
```


Setzt den Dateinamen (ohne Pfad), in dem die Schriftart gespeichert wird.

 **Remarks:** 

Diese Eigenschaft ermöglicht es Ihnen, die Art und Weise, wie Schriftdateinamen beim Export nach HTML erzeugt werden, neu zu definieren.

Wenn das Ereignis ausgelöst wird, enthält diese Eigenschaft den von Aspose.Words erzeugten Dateinamen. Sie können den Wert dieser Eigenschaft ändern, um die Schriftart in einer anderen Datei zu speichern. Beachten Sie, dass Dateinamen eindeutig sein müssen.

Aspose.Words erzeugt beim Export in das HTML-Format automatisch einen eindeutigen Dateinamen für jede eingebettete Schriftart. Wie der Schriftdateiname erzeugt wird, hängt davon ab, ob Sie das Dokument in einer Datei oder in einem Stream speichern.

Beim Speichern eines Dokuments in einer Datei sieht der erzeugte Schriftdateiname wie *..* aus.

Beim Speichern eines Dokuments in einem Stream sieht der erzeugte Schriftdateiname wie *Aspose.Words...* aus.

[getFontFileName()](../../com.aspose.words/fontsavingargs/\#getFontFileName) / [setFontFileName(java.lang.String)](../../com.aspose.words/fontsavingargs/\#setFontFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving using the document file name, the [HtmlSaveOptions.getFontsFolder()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolder) / [HtmlSaveOptions.setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolder-java.lang.String) and [HtmlSaveOptions.getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions/\#getFontsFolderAlias) / [HtmlSaveOptions.setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions/\#setFontsFolderAlias-java.lang.String) properties.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für das Exportieren von Schriftarten beim Speichern nach HTML definiert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Dateiname (ohne Pfad), in dem die Schrift gespeichert wird. |

### setFontStream(OutputStream value) {#setFontStream-java.io.OutputStream}
```
public void setFontStream(OutputStream value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.io.OutputStream |  |

### setKeepFontStreamOpen(boolean value) {#setKeepFontStreamOpen-boolean}
```
public void setKeepFontStreamOpen(boolean value)
```


Legt fest, ob Aspose.Words den Stream nach dem Speichern einer Schriftart offen lassen oder schließen soll.

 **Remarks:** 

Standard ist  false  und Aspose.Words schließt den Stream, den Sie in der **P:Aspose.Words.Saving.FontSavingArgs.FontStream**-Eigenschaft angegeben haben, nachdem eine Schriftart darin geschrieben wurde. Geben Sie  true  an, um den Stream offen zu lassen.

 **Examples:** 

Zeigt, wie benutzerdefinierte Logik für das Exportieren von Schriftarten beim Speichern nach HTML definiert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

