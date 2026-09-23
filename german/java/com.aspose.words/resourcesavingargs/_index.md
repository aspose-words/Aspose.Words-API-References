---
title: "ResourceSavingArgs"
linktitle: "ResourceSavingArgs"
second_title: "Aspose.Words für Java"
description: "Stellt Daten für das IResourceSavingCallback.resourceSavingcom.aspose.words.ResourceSavingArgs-Ereignis in Java bereit."
type: docs
weight: 577
url: /de/java/com.aspose.words/resourcesavingargs/
---

**Inheritance:**
java.lang.Object
```
public class ResourceSavingArgs
```

Stellt Daten für das [IResourceSavingCallback.resourceSaving(com.aspose.words.ResourceSavingArgs)](../../com.aspose.words/iresourcesavingcallback/\#resourceSaving-com.aspose.words.ResourceSavingArgs) Ereignis bereit.

Um mehr zu erfahren, besuchen Sie den [ Save a Document ][Save a Document] Dokumentationsartikel.

 **Remarks:** 

Standardmäßig speichert Aspose.Words ein Dokument als festseitiges HTML, SVG oder Markdown und legt jede Ressource in einer separaten Datei ab. Aspose.Words verwendet den Dokumentdateinamen und eine eindeutige Nummer, um für jede im Dokument gefundene Ressource einen eindeutigen Dateinamen zu erzeugen.

[ResourceSavingArgs](../../com.aspose.words/resourcesavingargs/) allows to redefine how resource file names are generated or to completely circumvent saving of resources into files by providing your own stream objects.

Um Ihre eigene Logik zur Erzeugung von Ressourcendateinamen anzuwenden, verwenden Sie die [getResourceFileName()](../../com.aspose.words/resourcesavingargs/\#getResourceFileName) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs/\#setResourceFileName-java.lang.String)-Eigenschaft.

Um Ressourcen in Streams statt in Dateien zu speichern, verwenden Sie die **P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**‑Eigenschaft.

 **Examples:** 

Zeigt, wie man einen Callback verwendet, um externe Ressourcen zu verfolgen, die beim Konvertieren eines Dokuments zu HTML erstellt werden.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getDocument()](#getDocument) | Ermittelt das Dokumentobjekt, das gerade gespeichert wird. |
| [getKeepResourceStreamOpen()](#getKeepResourceStreamOpen) | Gibt an, ob Aspose.Words den Stream offen lassen oder nach dem Speichern einer Ressource schließen soll. |
| [getResourceFileName()](#getResourceFileName) | Ermittelt den Dateinamen (ohne Pfad), in dem die Ressource gespeichert wird. |
| [getResourceFileUri()](#getResourceFileUri) | Ermittelt den Uniform Resource Identifier (URI), der verwendet wird, um die Ressourcendatei aus dem Dokument zu referenzieren. |
| [getResourceStream()](#getResourceStream) |  |
| [setKeepResourceStreamOpen(boolean value)](#setKeepResourceStreamOpen-boolean) | Gibt an, ob Aspose.Words den Stream offen lassen oder nach dem Speichern einer Ressource schließen soll. |
| [setResourceFileName(String value)](#setResourceFileName-java.lang.String) | Legt den Dateinamen (ohne Pfad) fest, in dem die Ressource gespeichert wird. |
| [setResourceFileUri(String value)](#setResourceFileUri-java.lang.String) | Legt den Uniform Resource Identifier (URI) fest, der verwendet wird, um die Ressourcendatei aus dem Dokument zu referenzieren. |
| [setResourceStream(OutputStream value)](#setResourceStream-java.io.OutputStream) |  |
### getDocument() {#getDocument}
```
public Document getDocument()
```


Ermittelt das Dokumentobjekt, das gerade gespeichert wird.

 **Examples:** 

Zeigt, wie man einen Callback verwendet, um externe Ressourcen zu verfolgen, die beim Konvertieren eines Dokuments zu HTML erstellt werden.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```

**Returns:**
[Document](../../com.aspose.words/document/) - The document object that is currently being saved.
### getKeepResourceStreamOpen() {#getKeepResourceStreamOpen}
```
public boolean getKeepResourceStreamOpen()
```


Gibt an, ob Aspose.Words den Stream offen lassen oder nach dem Speichern einer Ressource schließen soll.

 **Remarks:** 

Standard ist  false  und Aspose.Words schließt den Stream, den Sie in der **P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**-Eigenschaft bereitgestellt haben, nachdem eine Ressource darin geschrieben wurde. Geben Sie  true  an, um den Stream offen zu lassen.

 **Examples:** 

Zeigt, wie man einen Callback verwendet, um die URIs externer Ressourcen auszugeben, die beim Konvertieren eines Dokuments zu HTML erstellt werden.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getResourceFileName() {#getResourceFileName}
```
public String getResourceFileName()
```


Ermittelt den Dateinamen (ohne Pfad), in dem die Ressource gespeichert wird.

 **Remarks:** 

Diese Eigenschaft ermöglicht es Ihnen, die Art und Weise, wie die Ressourcendateinamen beim Export zu festseitigem HTML, SVG oder Markdown erzeugt werden, neu zu definieren.

Wenn das Ereignis ausgelöst wird, enthält diese Eigenschaft den von Aspose.Words erzeugten Dateinamen. Sie können den Wert dieser Eigenschaft ändern, um die Ressource in einer anderen Datei zu speichern. Beachten Sie, dass Dateinamen eindeutig sein müssen.

Aspose.Words erzeugt beim Export in das festseitige HTML-, SVG- oder Markdown-Format automatisch für jede Ressource einen eindeutigen Dateinamen. Wie der Ressourcendateiname erzeugt wird, hängt davon ab, ob Sie das Dokument in einer Datei oder in einem Stream speichern.

Beim Speichern eines Dokuments in einer Datei sieht der erzeugte Ressourcendateiname etwa so aus: *.![Image 1][].*.

Beim Speichern eines Dokuments in einem Stream sieht der erzeugte Ressourcendateiname etwa so aus: *Aspose.Words..![Image 1][].*.

[getResourceFileName()](../../com.aspose.words/resourcesavingargs/\#getResourceFileName) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs/\#setResourceFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) or [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) and [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [MarkdownSaveOptions.getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [MarkdownSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) or [MarkdownSaveOptions.getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [MarkdownSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String)

 **Examples:** 

Zeigt, wie man einen Callback verwendet, um externe Ressourcen zu verfolgen, die beim Konvertieren eines Dokuments zu HTML erstellt werden.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**


[Image 1]: 

**Returns:**
java.lang.String – Der Dateiname (ohne Pfad), in dem die Ressource gespeichert wird.
### getResourceFileUri() {#getResourceFileUri}
```
public String getResourceFileUri()
```


Ermittelt den Uniform Resource Identifier (URI), der verwendet wird, um die Ressourcendatei aus dem Dokument zu referenzieren.

 **Remarks:** 

Diese Eigenschaft ermöglicht es Ihnen, die URIs von Ressourcendateien, die in festseitige HTML-, SVG- oder Markdown-Dokumente exportiert werden, zu ändern.

Aspose.Words erzeugt beim Export in das festseitige HTML-, SVG- oder Markdown-Format automatisch einen URI für jede Ressourcendatei. Die erzeugten URIs verweisen auf von Aspose.Words gespeicherte Ressourcendateien. Die URIs können jedoch falsch sein, wenn Ressourcendateien an einen anderen Ort verschoben werden oder wenn Ressourcendateien in Streams gespeichert werden. Diese Eigenschaft ermöglicht es, die URIs in diesen Fällen zu korrigieren.

Wenn das Ereignis ausgelöst wird, enthält diese Eigenschaft den von Aspose.Words erzeugten URI. Sie können den Wert dieser Eigenschaft ändern, um einen benutzerdefinierten URI für die Ressourcendatei bereitzustellen.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [MarkdownSaveOptions.getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [MarkdownSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) [MarkdownSaveOptions.getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [MarkdownSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String)

 **Examples:** 

Zeigt, wie man einen Callback verwendet, um externe Ressourcen zu verfolgen, die beim Konvertieren eines Dokuments zu HTML erstellt werden.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```

**Returns:**
java.lang.String – Der Uniform Resource Identifier (URI), der verwendet wird, um die Ressourcendatei aus dem Dokument zu referenzieren.
### getResourceStream() {#getResourceStream}
```
public OutputStream getResourceStream()
```




**Returns:**
java.io.OutputStream
### setKeepResourceStreamOpen(boolean value) {#setKeepResourceStreamOpen-boolean}
```
public void setKeepResourceStreamOpen(boolean value)
```


Gibt an, ob Aspose.Words den Stream offen lassen oder nach dem Speichern einer Ressource schließen soll.

 **Remarks:** 

Standard ist  false  und Aspose.Words schließt den Stream, den Sie in der **P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**-Eigenschaft bereitgestellt haben, nachdem eine Ressource darin geschrieben wurde. Geben Sie  true  an, um den Stream offen zu lassen.

 **Examples:** 

Zeigt, wie man einen Callback verwendet, um die URIs externer Ressourcen auszugeben, die beim Konvertieren eines Dokuments zu HTML erstellt werden.

```

 public void htmlFixedResourceFolder() throws Exception {
     Document doc = new Document(getMyDir() + "Rendering.docx");

     ResourceUriPrinter callback = new ResourceUriPrinter();

     HtmlFixedSaveOptions options = new HtmlFixedSaveOptions();
     {
         options.setSaveFormat(SaveFormat.HTML_FIXED);
         options.setExportEmbeddedImages(false);
         options.setResourcesFolder(getArtifactsDir() + "HtmlFixedResourceFolder");
         options.setResourcesFolderAlias(getArtifactsDir() + "HtmlFixedResourceFolderAlias");
         options.setShowPageBorder(false);
         options.setResourceSavingCallback(callback);
     }

     // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
     // We must ensure the folder exists before the streams can put their resources into it.
     new File(options.getResourcesFolderAlias()).mkdir();

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

     System.out.println(callback.getText());

     String[] resourceFiles = new File(getArtifactsDir() + "HtmlFixedResourceFolderAlias").list();

     Assert.assertFalse(new File(getArtifactsDir() + "HtmlFixedResourceFolder").exists());
     Assert.assertEquals(6, IterableUtils.countMatches(Arrays.asList(resourceFiles),
             f -> f.endsWith(".jpeg") || f.endsWith(".png") || f.endsWith(".css")));
 }

 /// 
 /// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
 /// 
 private static class ResourceUriPrinter implements IResourceSavingCallback {
     public void resourceSaving(ResourceSavingArgs args) throws Exception {
         // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
         mText.append(MessageFormat.format("Resource #{0} \"{1}\"", ++mSavedResourceCount, args.getResourceFileName()));

         String extension = FilenameUtils.getExtension(args.getResourceFileName());
         switch (extension) {
             case "ttf":
             case "woff": {
                 // By default, 'ResourceFileUri' uses system folder for fonts.
                 // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                 args.setResourceFileUri(getArtifactsDir() + File.separatorChar + args.getResourceFileName());
                 break;
             }
         }

         mText.append("\t" + args.getResourceFileUri());

         // If we have specified a folder in the "ResourcesFolderAlias" property,
         // we will also need to redirect each stream to put its resource in that folder.
         args.setResourceStream(new FileOutputStream(args.getResourceFileUri()));
         args.setKeepResourceStreamOpen(false);
     }

     public String getText() {
         return mText.toString();
     }

     private int mSavedResourceCount;
     private final  StringBuilder mText = new StringBuilder();
 }
 
```

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setResourceFileName(String value) {#setResourceFileName-java.lang.String}
```
public void setResourceFileName(String value)
```


Legt den Dateinamen (ohne Pfad) fest, in dem die Ressource gespeichert wird.

 **Remarks:** 

Diese Eigenschaft ermöglicht es Ihnen, die Art und Weise, wie die Ressourcendateinamen beim Export zu festseitigem HTML, SVG oder Markdown erzeugt werden, neu zu definieren.

Wenn das Ereignis ausgelöst wird, enthält diese Eigenschaft den von Aspose.Words erzeugten Dateinamen. Sie können den Wert dieser Eigenschaft ändern, um die Ressource in einer anderen Datei zu speichern. Beachten Sie, dass Dateinamen eindeutig sein müssen.

Aspose.Words erzeugt beim Export in das festseitige HTML-, SVG- oder Markdown-Format automatisch für jede Ressource einen eindeutigen Dateinamen. Wie der Ressourcendateiname erzeugt wird, hängt davon ab, ob Sie das Dokument in einer Datei oder in einem Stream speichern.

Beim Speichern eines Dokuments in einer Datei sieht der erzeugte Ressourcendateiname etwa so aus: *.![Image 1][].*.

Beim Speichern eines Dokuments in einem Stream sieht der erzeugte Ressourcendateiname etwa so aus: *Aspose.Words..![Image 1][].*.

[getResourceFileName()](../../com.aspose.words/resourcesavingargs/\#getResourceFileName) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs/\#setResourceFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) or [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) and [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [MarkdownSaveOptions.getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [MarkdownSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) or [MarkdownSaveOptions.getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [MarkdownSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String)

 **Examples:** 

Zeigt, wie man einen Callback verwendet, um externe Ressourcen zu verfolgen, die beim Konvertieren eines Dokuments zu HTML erstellt werden.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**


[Image 1]: 

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Dateiname (ohne Pfad), in dem die Ressource gespeichert wird. |

### setResourceFileUri(String value) {#setResourceFileUri-java.lang.String}
```
public void setResourceFileUri(String value)
```


Legt den Uniform Resource Identifier (URI) fest, der verwendet wird, um die Ressourcendatei aus dem Dokument zu referenzieren.

 **Remarks:** 

Diese Eigenschaft ermöglicht es Ihnen, die URIs von Ressourcendateien, die in festseitige HTML-, SVG- oder Markdown-Dokumente exportiert werden, zu ändern.

Aspose.Words erzeugt beim Export in das festseitige HTML-, SVG- oder Markdown-Format automatisch einen URI für jede Ressourcendatei. Die erzeugten URIs verweisen auf von Aspose.Words gespeicherte Ressourcendateien. Die URIs können jedoch falsch sein, wenn Ressourcendateien an einen anderen Ort verschoben werden oder wenn Ressourcendateien in Streams gespeichert werden. Diese Eigenschaft ermöglicht es, die URIs in diesen Fällen zu korrigieren.

Wenn das Ereignis ausgelöst wird, enthält diese Eigenschaft den von Aspose.Words erzeugten URI. Sie können den Wert dieser Eigenschaft ändern, um einen benutzerdefinierten URI für die Ressourcendatei bereitzustellen.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [MarkdownSaveOptions.getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [MarkdownSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) [MarkdownSaveOptions.getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [MarkdownSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String)

 **Examples:** 

Zeigt, wie man einen Callback verwendet, um externe Ressourcen zu verfolgen, die beim Konvertieren eines Dokuments zu HTML erstellt werden.

```

 public void resourceSavingCallback() throws Exception {
     Document doc = new Document(getMyDir() + "Bullet points with alternative font.docx");

     FontSavingCallback callback = new FontSavingCallback();

     HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
     {
         saveOptions.setResourceSavingCallback(callback);
     }

     doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

     System.out.println(callback.getText());
 }

 private static class FontSavingCallback implements IResourceSavingCallback {
     /// 
     /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
     /// 
     public void resourceSaving(ResourceSavingArgs args) {
         mText.append(MessageFormat.format("Original document URI:\t{0}", args.getDocument().getOriginalFileName()));
         mText.append(MessageFormat.format("Resource being saved:\t{0}", args.getResourceFileName()));
         mText.append(MessageFormat.format("Full uri after saving:\t{0}\n", args.getResourceFileUri()));
     }

     public String getText() {
         return mText.toString();
     }

     private final StringBuilder mText = new StringBuilder();
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Uniform Resource Identifier (URI), der verwendet wird, um die Ressourcendatei aus dem Dokument zu referenzieren. |

### setResourceStream(OutputStream value) {#setResourceStream-java.io.OutputStream}
```
public void setResourceStream(OutputStream value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.io.OutputStream |  |

