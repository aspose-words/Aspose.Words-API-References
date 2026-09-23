---
title: "ResourceSavingArgs"
linktitle: "ResourceSavingArgs"
second_title: "Aspose.Words pour Java"
description: "Fournit des données pour le IResourceSavingCallback.resourceSavingcom.aspose.words.ResourceSavingArgs événement en Java."
type: docs
weight: 577
url: /fr/java/com.aspose.words/resourcesavingargs/
---

**Inheritance:**
java.lang.Object
```
public class ResourceSavingArgs
```

Fournit des données pour le [IResourceSavingCallback.resourceSaving(com.aspose.words.ResourceSavingArgs)](../../com.aspose.words/iresourcesavingcallback/\#resourceSaving-com.aspose.words.ResourceSavingArgs) événement.

Pour en savoir plus, consultez l'article de documentation [ Save a Document ][Save a Document].

 **Remarks:** 

Par défaut, lorsque Aspose.Words enregistre un document au format HTML à page fixe, SVG ou Markdown, il enregistre chaque ressource dans un fichier séparé. Aspose.Words utilise le nom de fichier du document et un numéro unique pour générer un nom de fichier unique pour chaque ressource trouvée dans le document.

[ResourceSavingArgs](../../com.aspose.words/resourcesavingargs/) allows to redefine how resource file names are generated or to completely circumvent saving of resources into files by providing your own stream objects.

Pour appliquer votre propre logique de génération des noms de fichiers de ressources, utilisez la propriété [getResourceFileName()](../../com.aspose.words/resourcesavingargs/\#getResourceFileName) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs/\#setResourceFileName-java.lang.String).

Pour enregistrer les ressources dans des flux au lieu de fichiers, utilisez la propriété **P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**.

 **Examples:** 

Montre comment utiliser un rappel pour suivre les ressources externes créées lors de la conversion d'un document en HTML.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getDocument()](#getDocument) | Obtient l'objet document qui est actuellement en cours d'enregistrement. |
| [getKeepResourceStreamOpen()](#getKeepResourceStreamOpen) | Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement d'une ressource. |
| [getResourceFileName()](#getResourceFileName) | Obtient le nom de fichier (sans le chemin) où la ressource sera enregistrée. |
| [getResourceFileUri()](#getResourceFileUri) | Obtient l'identifiant uniforme de ressource (URI) utilisé pour référencer le fichier de ressource depuis le document. |
| [getResourceStream()](#getResourceStream) |  |
| [setKeepResourceStreamOpen(boolean value)](#setKeepResourceStreamOpen-boolean) | Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement d'une ressource. |
| [setResourceFileName(String value)](#setResourceFileName-java.lang.String) | Définit le nom de fichier (sans le chemin) où la ressource sera enregistrée. |
| [setResourceFileUri(String value)](#setResourceFileUri-java.lang.String) | Définit l'identifiant uniforme de ressource (URI) utilisé pour référencer le fichier de ressource depuis le document. |
| [setResourceStream(OutputStream value)](#setResourceStream-java.io.OutputStream) |  |
### getDocument() {#getDocument}
```
public Document getDocument()
```


Obtient l'objet document qui est actuellement en cours d'enregistrement.

 **Examples:** 

Montre comment utiliser un rappel pour suivre les ressources externes créées lors de la conversion d'un document en HTML.

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


Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement d'une ressource.

 **Remarks:** 

Par défaut, la valeur est  false  et Aspose.Words fermera le flux que vous avez fourni dans la propriété **P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** après y avoir écrit une ressource. Spécifiez  true  pour garder le flux ouvert.

 **Examples:** 

Montre comment utiliser un rappel pour afficher les URI des ressources externes créées lors de la conversion d'un document en HTML.

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
boolean - La valeur  boolean  correspondante.
### getResourceFileName() {#getResourceFileName}
```
public String getResourceFileName()
```


Obtient le nom de fichier (sans le chemin) où la ressource sera enregistrée.

 **Remarks:** 

Cette propriété vous permet de redéfinir la façon dont les noms de fichiers de ressources sont générés lors de l'exportation vers HTML à page fixe, SVG ou Markdown.

Lorsque l'événement est déclenché, cette propriété contient le nom de fichier qui a été généré par Aspose.Words. Vous pouvez modifier la valeur de cette propriété pour enregistrer la ressource dans un fichier différent. Notez que les noms de fichiers doivent être uniques.

Aspose.Words génère automatiquement un nom de fichier unique pour chaque ressource lors de l'exportation vers le format HTML à page fixe, SVG ou Markdown. La façon dont le nom de fichier de la ressource est généré dépend de si vous enregistrez le document dans un fichier ou dans un flux.

Lors de l'enregistrement d'un document dans un fichier, le nom de fichier de ressource généré ressemble à *.![Image 1][].*.

Lors de l'enregistrement d'un document dans un flux, le nom de fichier de ressource généré ressemble à *Aspose.Words..![Image 1][].*.

[getResourceFileName()](../../com.aspose.words/resourcesavingargs/\#getResourceFileName) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs/\#setResourceFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) or [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) and [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [MarkdownSaveOptions.getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [MarkdownSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) or [MarkdownSaveOptions.getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [MarkdownSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String)

 **Examples:** 

Montre comment utiliser un rappel pour suivre les ressources externes créées lors de la conversion d'un document en HTML.

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
java.lang.String - Le nom de fichier (sans le chemin) où la ressource sera enregistrée.
### getResourceFileUri() {#getResourceFileUri}
```
public String getResourceFileUri()
```


Obtient l'identifiant uniforme de ressource (URI) utilisé pour référencer le fichier de ressource depuis le document.

 **Remarks:** 

Cette propriété vous permet de modifier les URI des fichiers de ressources exportés vers des documents HTML à page fixe, SVG ou Markdown.

Aspose.Words génère automatiquement une URI pour chaque fichier de ressource lors de l'exportation vers le format HTML à page fixe, SVG ou Markdown. Les URI générées font référence aux fichiers de ressources enregistrés par Aspose.Words. Cependant, les URI peuvent être incorrectes si les fichiers de ressources sont déplacés vers un autre emplacement ou si les fichiers de ressources sont enregistrés dans des flux. Cette propriété permet de corriger les URI dans ces cas.

Lorsque l'événement est déclenché, cette propriété contient l'URI qui a été générée par Aspose.Words. Vous pouvez modifier la valeur de cette propriété pour fournir une URI personnalisée pour le fichier de ressource.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [MarkdownSaveOptions.getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [MarkdownSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) [MarkdownSaveOptions.getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [MarkdownSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String)

 **Examples:** 

Montre comment utiliser un rappel pour suivre les ressources externes créées lors de la conversion d'un document en HTML.

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
java.lang.String - L'identifiant uniforme de ressource (URI) utilisé pour référencer le fichier de ressource depuis le document.
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


Spécifie si Aspose.Words doit garder le flux ouvert ou le fermer après l'enregistrement d'une ressource.

 **Remarks:** 

Par défaut, la valeur est  false  et Aspose.Words fermera le flux que vous avez fourni dans la propriété **P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** après y avoir écrit une ressource. Spécifiez  true  pour garder le flux ouvert.

 **Examples:** 

Montre comment utiliser un rappel pour afficher les URI des ressources externes créées lors de la conversion d'un document en HTML.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setResourceFileName(String value) {#setResourceFileName-java.lang.String}
```
public void setResourceFileName(String value)
```


Définit le nom de fichier (sans le chemin) où la ressource sera enregistrée.

 **Remarks:** 

Cette propriété vous permet de redéfinir la façon dont les noms de fichiers de ressources sont générés lors de l'exportation vers HTML à page fixe, SVG ou Markdown.

Lorsque l'événement est déclenché, cette propriété contient le nom de fichier qui a été généré par Aspose.Words. Vous pouvez modifier la valeur de cette propriété pour enregistrer la ressource dans un fichier différent. Notez que les noms de fichiers doivent être uniques.

Aspose.Words génère automatiquement un nom de fichier unique pour chaque ressource lors de l'exportation vers le format HTML à page fixe, SVG ou Markdown. La façon dont le nom de fichier de la ressource est généré dépend de si vous enregistrez le document dans un fichier ou dans un flux.

Lors de l'enregistrement d'un document dans un fichier, le nom de fichier de ressource généré ressemble à *.![Image 1][].*.

Lors de l'enregistrement d'un document dans un flux, le nom de fichier de ressource généré ressemble à *Aspose.Words..![Image 1][].*.

[getResourceFileName()](../../com.aspose.words/resourcesavingargs/\#getResourceFileName) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs/\#setResourceFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) or [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) and [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [MarkdownSaveOptions.getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [MarkdownSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) or [MarkdownSaveOptions.getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [MarkdownSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String) properties.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String)

 **Examples:** 

Montre comment utiliser un rappel pour suivre les ressources externes créées lors de la conversion d'un document en HTML.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | Le nom de fichier (sans le chemin) où la ressource sera enregistrée. |

### setResourceFileUri(String value) {#setResourceFileUri-java.lang.String}
```
public void setResourceFileUri(String value)
```


Définit l'identifiant uniforme de ressource (URI) utilisé pour référencer le fichier de ressource depuis le document.

 **Remarks:** 

Cette propriété vous permet de modifier les URI des fichiers de ressources exportés vers des documents HTML à page fixe, SVG ou Markdown.

Aspose.Words génère automatiquement une URI pour chaque fichier de ressource lors de l'exportation vers le format HTML à page fixe, SVG ou Markdown. Les URI générées font référence aux fichiers de ressources enregistrés par Aspose.Words. Cependant, les URI peuvent être incorrectes si les fichiers de ressources sont déplacés vers un autre emplacement ou si les fichiers de ressources sont enregistrés dans des flux. Cette propriété permet de corriger les URI dans ces cas.

Lorsque l'événement est déclenché, cette propriété contient l'URI qui a été générée par Aspose.Words. Vous pouvez modifier la valeur de cette propriété pour fournir une URI personnalisée pour le fichier de ressource.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [MarkdownSaveOptions.getImagesFolder()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolder) / [MarkdownSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) [MarkdownSaveOptions.getImagesFolderAlias()](../../com.aspose.words/markdownsaveoptions/\#getImagesFolderAlias) / [MarkdownSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/markdownsaveoptions/\#setImagesFolderAlias-java.lang.String)

 **Examples:** 

Montre comment utiliser un rappel pour suivre les ressources externes créées lors de la conversion d'un document en HTML.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | L'identifiant uniforme de ressource (URI) utilisé pour référencer le fichier de ressource depuis le document. |

### setResourceStream(OutputStream value) {#setResourceStream-java.io.OutputStream}
```
public void setResourceStream(OutputStream value)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.io.OutputStream |  |

