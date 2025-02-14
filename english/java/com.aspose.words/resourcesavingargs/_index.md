---
title: ResourceSavingArgs
linktitle: ResourceSavingArgs
second_title: Aspose.Words for Java
description: Provides data for the IResourceSavingCallback.resourceSavingcom.aspose.words.ResourceSavingArgs event in Java.
type: docs
weight: 557
url: /java/com.aspose.words/resourcesavingargs/
---

**Inheritance:**
java.lang.Object
```
public class ResourceSavingArgs
```

Provides data for the [IResourceSavingCallback.resourceSaving(com.aspose.words.ResourceSavingArgs)](../../com.aspose.words/iresourcesavingcallback/\#resourceSaving-com.aspose.words.ResourceSavingArgs) event.

To learn more, visit the [ Save a Document ][Save a Document] documentation article.

 **Remarks:** 

By default, when Aspose.Words saves a document to fixed page HTML or SVG, it saves each resource into a separate file. Aspose.Words uses the document file name and a unique number to generate unique file name for each resource found in the document.

[ResourceSavingArgs](../../com.aspose.words/resourcesavingargs/) allows to redefine how resource file names are generated or to completely circumvent saving of resources into files by providing your own stream objects.

To apply your own logic for generating resource file names use the [getResourceFileName()](../../com.aspose.words/resourcesavingargs/\#getResourceFileName) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs/\#setResourceFileName-java.lang.String) property.

To save resources into streams instead of files, use the **P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** property.

 **Examples:** 

Shows how to use a callback to track external resources created while converting a document to HTML.

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
## Methods

| Method | Description |
| --- | --- |
| [getDocument()](#getDocument) | Gets the document object that is currently being saved. |
| [getKeepResourceStreamOpen()](#getKeepResourceStreamOpen) | Specifies whether Aspose.Words should keep the stream open or close it after saving a resource. |
| [getResourceFileName()](#getResourceFileName) | Gets the file name (without path) where the resource will be saved to. |
| [getResourceFileUri()](#getResourceFileUri) | Gets the uniform resource identifier (URI) used to reference the resource file from the document. |
| [getResourceStream()](#getResourceStream) |  |
| [setKeepResourceStreamOpen(boolean value)](#setKeepResourceStreamOpen-boolean) | Specifies whether Aspose.Words should keep the stream open or close it after saving a resource. |
| [setResourceFileName(String value)](#setResourceFileName-java.lang.String) | Sets the file name (without path) where the resource will be saved to. |
| [setResourceFileUri(String value)](#setResourceFileUri-java.lang.String) | Sets the uniform resource identifier (URI) used to reference the resource file from the document. |
| [setResourceStream(OutputStream value)](#setResourceStream-java.io.OutputStream) |  |
### getDocument() {#getDocument}
```
public Document getDocument()
```


Gets the document object that is currently being saved.

 **Examples:** 

Shows how to use a callback to track external resources created while converting a document to HTML.

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


Specifies whether Aspose.Words should keep the stream open or close it after saving a resource.

 **Remarks:** 

Default is  false  and Aspose.Words will close the stream you provided in the **P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** property after writing a resource into it. Specify  true  to keep the stream open.

 **Examples:** 

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML.

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
boolean - The corresponding  boolean  value.
### getResourceFileName() {#getResourceFileName}
```
public String getResourceFileName()
```


Gets the file name (without path) where the resource will be saved to.

 **Remarks:** 

This property allows you to redefine how the resource file names are generated during export to fixed page HTML or SVG.

When the event is fired, this property contains the file name that was generated by Aspose.Words. You can change the value of this property to save the resource into a different file. Note that file names must be unique.

Aspose.Words automatically generates a unique file name for every resource when exporting to fixed page HTML or SVG format. How the resource file name is generated depends on whether you save the document to a file or to a stream.

When saving a document to a file, the generated resource file name looks like *.![Image 1][].*.

When saving a document to a stream, the generated resource file name looks like *Aspose.Words..![Image 1][].*.

[getResourceFileName()](../../com.aspose.words/resourcesavingargs/\#getResourceFileName) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs/\#setResourceFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to fixed page HTML or SVG using the document file name, the [HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) or [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) and [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) properties.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String)

 **Examples:** 

Shows how to use a callback to track external resources created while converting a document to HTML.

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
java.lang.String - The file name (without path) where the resource will be saved to.
### getResourceFileUri() {#getResourceFileUri}
```
public String getResourceFileUri()
```


Gets the uniform resource identifier (URI) used to reference the resource file from the document.

 **Remarks:** 

This property allows you to change URIs of resource files exported to fixed page HTML or SVG documents.

Aspose.Words automatically generates an URI for every resource file during export to fixed page HTML or SVG format. The generated URIs reference resource files saved by Aspose.Words. However, the URIs can be incorrect if resource files are to be moved to other location or if resource files are saved to streams. This property allows to correct URIs in these cases.

When the event is fired, this property contains the URI that was generated by Aspose.Words. You can change the value of this property to provide a custom URI for the resource file.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String)

 **Examples:** 

Shows how to use a callback to track external resources created while converting a document to HTML.

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
java.lang.String - The uniform resource identifier (URI) used to reference the resource file from the document.
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


Specifies whether Aspose.Words should keep the stream open or close it after saving a resource.

 **Remarks:** 

Default is  false  and Aspose.Words will close the stream you provided in the **P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** property after writing a resource into it. Specify  true  to keep the stream open.

 **Examples:** 

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setResourceFileName(String value) {#setResourceFileName-java.lang.String}
```
public void setResourceFileName(String value)
```


Sets the file name (without path) where the resource will be saved to.

 **Remarks:** 

This property allows you to redefine how the resource file names are generated during export to fixed page HTML or SVG.

When the event is fired, this property contains the file name that was generated by Aspose.Words. You can change the value of this property to save the resource into a different file. Note that file names must be unique.

Aspose.Words automatically generates a unique file name for every resource when exporting to fixed page HTML or SVG format. How the resource file name is generated depends on whether you save the document to a file or to a stream.

When saving a document to a file, the generated resource file name looks like *.![Image 1][].*.

When saving a document to a stream, the generated resource file name looks like *Aspose.Words..![Image 1][].*.

[getResourceFileName()](../../com.aspose.words/resourcesavingargs/\#getResourceFileName) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs/\#setResourceFileName-java.lang.String) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the  src  attribute for writing to fixed page HTML or SVG using the document file name, the [HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) or [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) and [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) or [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String) properties.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String)

 **Examples:** 

Shows how to use a callback to track external resources created while converting a document to HTML.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The file name (without path) where the resource will be saved to. |

### setResourceFileUri(String value) {#setResourceFileUri-java.lang.String}
```
public void setResourceFileUri(String value)
```


Sets the uniform resource identifier (URI) used to reference the resource file from the document.

 **Remarks:** 

This property allows you to change URIs of resource files exported to fixed page HTML or SVG documents.

Aspose.Words automatically generates an URI for every resource file during export to fixed page HTML or SVG format. The generated URIs reference resource files saved by Aspose.Words. However, the URIs can be incorrect if resource files are to be moved to other location or if resource files are saved to streams. This property allows to correct URIs in these cases.

When the event is fired, this property contains the URI that was generated by Aspose.Words. You can change the value of this property to provide a custom URI for the resource file.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolder) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolder-java.lang.String) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolder) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolder-java.lang.String) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions/\#getResourcesFolderAlias) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions/\#setResourcesFolderAlias-java.lang.String) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions/\#getResourcesFolderAlias) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions/\#setResourcesFolderAlias-java.lang.String)

 **Examples:** 

Shows how to use a callback to track external resources created while converting a document to HTML.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The uniform resource identifier (URI) used to reference the resource file from the document. |

### setResourceStream(OutputStream value) {#setResourceStream-java.io.OutputStream}
```
public void setResourceStream(OutputStream value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.io.OutputStream |  |

