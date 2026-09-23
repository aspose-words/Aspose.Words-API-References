---
title: "IResourceSavingCallback"
linktitle: "IResourceSavingCallback"
second_title: "Aspose.Words для Java"
description: "Реализуйте этот интерфейс, если хотите контролировать, как Aspose.Words сохраняет внешние ресурсы (изображения, шрифты и CSS) при сохранении документа в фиксированный HTML или SVG в Java."
type: docs
weight: 783
url: /ru/java/com.aspose.words/iresourcesavingcallback/
---
```
public interface IResourceSavingCallback
```

Реализуйте этот интерфейс, если вы хотите контролировать, как Aspose.Words сохраняет внешние ресурсы (изображения, шрифты и CSS) при сохранении документа в фиксированный HTML или SVG.

 **Examples:** 

Показывает, как использовать обратный вызов для отслеживания внешних ресурсов, создаваемых при конвертации документа в HTML.

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

Показывает, как использовать обратный вызов для вывода URI внешних ресурсов, создаваемых при конвертации документа в HTML.

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

Показывает, как использовать обратный вызов для изменения URI ресурса.

```

 public void resourceSavingCallback() throws Exception
 {
     String outputPath = getArtifactsDir() + "MarkdownSaveOptions.ResourceSavingCallback.md";

     Document doc = new Document(getMyDir() + "Rendering.docx");

     MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
     saveOptions.setResourceSavingCallback(new ChangeUriPath());

     doc.save(outputPath, saveOptions);

     DocumentHelper.findTextInFile(outputPath, "/uri/for/");
 }

 /// 
 /// Class implementing .
 /// 
 private static class ChangeUriPath implements IResourceSavingCallback
 {
     public void resourceSaving(ResourceSavingArgs args)
     {
         args.setResourceFileUri(MessageFormat.format("/uri/for/{0}", args.getResourceFileName()));
     }
 }
 
```
## Методы

| Метод | Описание |
| --- | --- |
| [resourceSaving(ResourceSavingArgs args)](#resourceSaving-com.aspose.words.ResourceSavingArgs) | Вызывается, когда Aspose.Words сохраняет внешний ресурс в фиксированный HTML или SVG. |
### resourceSaving(ResourceSavingArgs args) {#resourceSaving-com.aspose.words.ResourceSavingArgs}
```
public abstract void resourceSaving(ResourceSavingArgs args)
```


Вызывается, когда Aspose.Words сохраняет внешний ресурс в фиксированный HTML или SVG.

 **Examples:** 

Показывает, как использовать обратный вызов для отслеживания внешних ресурсов, создаваемых при конвертации документа в HTML.

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

Показывает, как использовать обратный вызов для вывода URI внешних ресурсов, создаваемых при конвертации документа в HTML.

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

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| args | [ResourceSavingArgs](../../com.aspose.words/resourcesavingargs/) |  |

