---
title: "IResourceLoadingCallback"
linktitle: "IResourceLoadingCallback"
second_title: "Aspose.Words für Java"
description: "Implementieren Sie dieses Interface, wenn Sie steuern möchten, wie Aspose.Words externe Ressourcen lädt, wenn ein Dokument importiert und Bilder mit DocumentBuilder in Java eingefügt werden."
type: docs
weight: 782
url: /de/java/com.aspose.words/iresourceloadingcallback/
---
```
public interface IResourceLoadingCallback
```

Implementieren Sie dieses Interface, wenn Sie steuern möchten, wie Aspose.Words externe Ressourcen lädt, wenn ein Dokument importiert und Bilder mit [DocumentBuilder](../../com.aspose.words/documentbuilder/) eingefügt werden.

 **Examples:** 

Zeigt, wie man den Vorgang des Ladens externer Ressourcen in ein Dokument anpasst.

```

 public void resourceLoadingCallback() throws Exception {
     Document doc = new Document();
     doc.setResourceLoadingCallback(new ImageNameHandler());

     DocumentBuilder builder = new DocumentBuilder(doc);

     // Images usually are inserted using a URI, or a byte array.
     // Every instance of a resource load will call our callback's ResourceLoading method.
     builder.insertImage("Google logo");
     builder.insertImage("Aspose logo");
     builder.insertImage("Watermark");

     Assert.assertEquals(3, doc.getChildNodes(NodeType.SHAPE, true).getCount());

     doc.save(getArtifactsDir() + "DocumentBase.ResourceLoadingCallback.docx");
 }

 /// 
 /// Allows us to load images into a document using predefined shorthands, as opposed to URIs.
 /// This will separate image loading logic from the rest of the document construction.
 /// 
 private static class ImageNameHandler implements IResourceLoadingCallback {
     public int resourceLoading(final ResourceLoadingArgs args) throws URISyntaxException, IOException {
         if (args.getResourceType() == ResourceType.IMAGE) {
             // If this callback encounters one of the image shorthands while loading an image,
             // it will apply unique logic for each defined shorthand instead of treating it as a URI.
             if ("Google logo".equals(args.getOriginalUri())) {
                 args.setData(DocumentHelper.getBytesFromStream(getImageUri().toURL().openStream()));

                 return ResourceLoadingAction.USER_PROVIDED;
             }

             if ("Aspose logo".equals(args.getOriginalUri())) {
                 args.setData(DocumentHelper.getBytesFromStream(getImageUri().toURL().openStream()));

                 return ResourceLoadingAction.USER_PROVIDED;
             }

             if ("Watermark".equals(args.getOriginalUri())) {
                 InputStream imageStream = new FileInputStream(getImageDir() + "Transparent background logo.png");
                 args.setData(DocumentHelper.getBytesFromStream(imageStream));

                 return ResourceLoadingAction.USER_PROVIDED;
             }
         }

         return ResourceLoadingAction.DEFAULT;
     }
 }
 
```
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [resourceLoading(ResourceLoadingArgs args)](#resourceLoading-com.aspose.words.ResourceLoadingArgs) | Wird aufgerufen, wenn Aspose.Words irgendeine externe Ressource lädt. |
### resourceLoading(ResourceLoadingArgs args) {#resourceLoading-com.aspose.words.ResourceLoadingArgs}
```
public abstract int resourceLoading(ResourceLoadingArgs args)
```


Wird aufgerufen, wenn Aspose.Words irgendeine externe Ressource lädt.

 **Examples:** 

Zeigt, wie man den Vorgang des Ladens externer Ressourcen in ein Dokument anpasst.

```

 public void resourceLoadingCallback() throws Exception {
     Document doc = new Document();
     doc.setResourceLoadingCallback(new ImageNameHandler());

     DocumentBuilder builder = new DocumentBuilder(doc);

     // Images usually are inserted using a URI, or a byte array.
     // Every instance of a resource load will call our callback's ResourceLoading method.
     builder.insertImage("Google logo");
     builder.insertImage("Aspose logo");
     builder.insertImage("Watermark");

     Assert.assertEquals(3, doc.getChildNodes(NodeType.SHAPE, true).getCount());

     doc.save(getArtifactsDir() + "DocumentBase.ResourceLoadingCallback.docx");
 }

 /// 
 /// Allows us to load images into a document using predefined shorthands, as opposed to URIs.
 /// This will separate image loading logic from the rest of the document construction.
 /// 
 private static class ImageNameHandler implements IResourceLoadingCallback {
     public int resourceLoading(final ResourceLoadingArgs args) throws URISyntaxException, IOException {
         if (args.getResourceType() == ResourceType.IMAGE) {
             // If this callback encounters one of the image shorthands while loading an image,
             // it will apply unique logic for each defined shorthand instead of treating it as a URI.
             if ("Google logo".equals(args.getOriginalUri())) {
                 args.setData(DocumentHelper.getBytesFromStream(getImageUri().toURL().openStream()));

                 return ResourceLoadingAction.USER_PROVIDED;
             }

             if ("Aspose logo".equals(args.getOriginalUri())) {
                 args.setData(DocumentHelper.getBytesFromStream(getImageUri().toURL().openStream()));

                 return ResourceLoadingAction.USER_PROVIDED;
             }

             if ("Watermark".equals(args.getOriginalUri())) {
                 InputStream imageStream = new FileInputStream(getImageDir() + "Transparent background logo.png");
                 args.setData(DocumentHelper.getBytesFromStream(imageStream));

                 return ResourceLoadingAction.USER_PROVIDED;
             }
         }

         return ResourceLoadingAction.DEFAULT;
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| args | [ResourceLoadingArgs](../../com.aspose.words/resourceloadingargs/) |  |

**Returns:**
int
