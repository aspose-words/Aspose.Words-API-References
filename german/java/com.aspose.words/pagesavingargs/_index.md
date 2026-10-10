---
title: "PageSavingArgs"
linktitle: "PageSavingArgs"
second_title: "Aspose.Words für Java"
description: "Stellt Daten für das Ereignis IPageSavingCallback.pageSavingcom.aspose.words.PageSavingArgs in Java bereit."
type: docs
weight: 517
url: /de/java/com.aspose.words/pagesavingargs/
---

**Inheritance:**
java.lang.Object
```
public class PageSavingArgs
```

Stellt Daten für das Ereignis [IPageSavingCallback.pageSaving(com.aspose.words.PageSavingArgs)](../../com.aspose.words/ipagesavingcallback/\#pageSaving-com.aspose.words.PageSavingArgs) bereit.

Weitere Informationen finden Sie im Dokumentationsartikel [ Programming with Documents ][Programming with Documents].

 **Examples:** 

Zeigt, wie man einen Callback verwendet, um ein Dokument seitenweise als HTML zu speichern.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getKeepPageStreamOpen()](#getKeepPageStreamOpen) | Gibt an, ob Aspose.Words den Stream nach dem Speichern einer Dokumentenseite offen halten oder schließen soll. |
| [getPageFileName()](#getPageFileName) | Ermittelt den Dateinamen, in dem die Dokumentenseite gespeichert wird. |
| [getPageIndex()](#getPageIndex) | Aktueller Seitenindex. |
| [getPageStream()](#getPageStream) |  |
| [setKeepPageStreamOpen(boolean value)](#setKeepPageStreamOpen-boolean) | Gibt an, ob Aspose.Words den Stream nach dem Speichern einer Dokumentenseite offen halten oder schließen soll. |
| [setPageFileName(String value)](#setPageFileName-java.lang.String) | Legt den Dateinamen fest, in dem die Dokumentenseite gespeichert wird. |
| [setPageStream(OutputStream value)](#setPageStream-java.io.OutputStream) |  |
### getKeepPageStreamOpen() {#getKeepPageStreamOpen}
```
public boolean getKeepPageStreamOpen()
```


Gibt an, ob Aspose.Words den Stream nach dem Speichern einer Dokumentenseite offen halten oder schließen soll.

 **Remarks:** 

Standard ist  false  und Aspose.Words schließt den Stream, den Sie in der Eigenschaft **P:Aspose.Words.Saving.PageSavingArgs.PageStream** bereitgestellt haben, nachdem eine Dokumentenseite darin geschrieben wurde. Geben Sie  true  an, um den Stream offen zu halten.

 **Examples:** 

Zeigt, wie man einen Callback verwendet, um ein Dokument seitenweise als HTML zu speichern.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```

**P:Aspose.Words.Saving.PageSavingArgs.PageStream**

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getPageFileName() {#getPageFileName}
```
public String getPageFileName()
```


Ermittelt den Dateinamen, in dem die Dokumentenseite gespeichert wird.

 **Remarks:** 

Wenn nicht angegeben, werden Dateiname und Pfad der Seite automatisch anhand des ursprünglichen Dateinamens generiert.

 **Examples:** 

Zeigt, wie man einen Callback verwendet, um ein Dokument seitenweise als HTML zu speichern.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```

**Returns:**
java.lang.String - Der Dateiname, unter dem die Dokumentseite gespeichert wird.
### getPageIndex() {#getPageIndex}
```
public int getPageIndex()
```


Aktueller Seitenindex.

 **Examples:** 

Zeigt, wie man einen Callback verwendet, um ein Dokument seitenweise als HTML zu speichern.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```

**Returns:**
int - Der entsprechende int-Wert.
### getPageStream() {#getPageStream}
```
public OutputStream getPageStream()
```




**Returns:**
java.io.OutputStream
### setKeepPageStreamOpen(boolean value) {#setKeepPageStreamOpen-boolean}
```
public void setKeepPageStreamOpen(boolean value)
```


Gibt an, ob Aspose.Words den Stream nach dem Speichern einer Dokumentenseite offen halten oder schließen soll.

 **Remarks:** 

Standard ist  false  und Aspose.Words schließt den Stream, den Sie in der Eigenschaft **P:Aspose.Words.Saving.PageSavingArgs.PageStream** bereitgestellt haben, nachdem eine Dokumentenseite darin geschrieben wurde. Geben Sie  true  an, um den Stream offen zu halten.

 **Examples:** 

Zeigt, wie man einen Callback verwendet, um ein Dokument seitenweise als HTML zu speichern.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```

**P:Aspose.Words.Saving.PageSavingArgs.PageStream**

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setPageFileName(String value) {#setPageFileName-java.lang.String}
```
public void setPageFileName(String value)
```


Legt den Dateinamen fest, in dem die Dokumentenseite gespeichert wird.

 **Remarks:** 

Wenn nicht angegeben, werden Dateiname und Pfad der Seite automatisch anhand des ursprünglichen Dateinamens generiert.

 **Examples:** 

Zeigt, wie man einen Callback verwendet, um ein Dokument seitenweise als HTML zu speichern.

```

 public void pageFileNames() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     builder.writeln("Page 1.");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 2.");
     builder.insertImage(getImageDir() + "Logo.jpg");
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.writeln("Page 3.");

     // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
     // to modify how we convert the document to HTML.
     HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

     // We will save each page in this document to a separate HTML file in the local file system.
     // Set a callback that allows us to name each output HTML document.
     htmlFixedSaveOptions.setPageSavingCallback(new CustomFileNamePageSavingCallback());

     doc.save(getArtifactsDir() + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

     String[] filePaths = DocumentHelper.directoryGetFiles(getArtifactsDir(), "SavingCallback.PageFileNames.Page_*").toArray(new String[0]);

     Assert.assertEquals(3, filePaths.length);
 }

 /// 
 /// Saves all pages to a file and directory specified within.
 /// 
 private static class CustomFileNamePageSavingCallback implements IPageSavingCallback {
     public void pageSaving(PageSavingArgs args) throws Exception {
         String outFileName = MessageFormat.format("{0}SavingCallback.PageFileNames.Page_{1}.html", getArtifactsDir(), args.getPageIndex());

         // Below are two ways of specifying where Aspose.Words will save each page of the document.
         // 1 -  Set a filename for the output page file:
         args.setPageFileName(outFileName);

         // 2 -  Create a custom stream for the output page file:
         try (FileOutputStream outputStream = new FileOutputStream(outFileName)) {
             args.setPageStream(outputStream);
         }

         Assert.assertFalse(args.getKeepPageStreamOpen());
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Dateiname, unter dem die Dokumentseite gespeichert wird. |

### setPageStream(OutputStream value) {#setPageStream-java.io.OutputStream}
```
public void setPageStream(OutputStream value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.io.OutputStream |  |

