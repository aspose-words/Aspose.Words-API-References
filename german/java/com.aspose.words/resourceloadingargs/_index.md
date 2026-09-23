---
title: "ResourceLoadingArgs"
linktitle: "ResourceLoadingArgs"
second_title: "Aspose.Words für Java"
description: "Stellt Daten für die Methode IResourceLoadingCallback.resourceLoadingcom.aspose.words.ResourceLoadingArgs in Java bereit."
type: docs
weight: 576
url: /de/java/com.aspose.words/resourceloadingargs/
---

**Inheritance:**
java.lang.Object
```
public class ResourceLoadingArgs
```

Stellt Daten für die Methode [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) bereit.

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
| [getOriginalUri()](#getOriginalUri) | Ursprüngliche URI der Ressource, wie im importierten Dokument angegeben. |
| [getResourceType()](#getResourceType) | Typ der Ressource. |
| [getUri()](#getUri) | URI der Ressource, die zum Herunterladen verwendet wird, wenn [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) zurückgibt [ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction/\#DEFAULT). |
| [setData(byte[] data)](#setData-byte) | Legt benutzerbereitgestellte Daten der Ressource fest, die verwendet werden, wenn [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) zurückgibt [ResourceLoadingAction.USER\_PROVIDED](../../com.aspose.words/resourceloadingaction/\#USER-PROVIDED). |
| [setUri(String value)](#setUri-java.lang.String) | URI der Ressource, die zum Herunterladen verwendet wird, wenn [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) zurückgibt [ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction/\#DEFAULT). |
### getOriginalUri() {#getOriginalUri}
```
public String getOriginalUri()
```


Ursprüngliche URI der Ressource, wie im importierten Dokument angegeben.

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

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getResourceType() {#getResourceType}
```
public int getResourceType()
```


Typ der Ressource.

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

**Returns:**
int - Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der [ResourceType](../../com.aspose.words/resourcetype/)‑Konstanten.
### getUri() {#getUri}
```
public String getUri()
```


URI der Ressource, die zum Herunterladen verwendet wird, wenn [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) zurückgibt [ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction/\#DEFAULT).

Anfangs ist sie auf die absolute URI der Ressource gesetzt, aber der Benutzer kann sie auf einen beliebigen Wert neu definieren.

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### setData(byte[] data) {#setData-byte}
```
public void setData(byte[] data)
```


Legt benutzerbereitgestellte Daten der Ressource fest, die verwendet werden, wenn [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) zurückgibt [ResourceLoadingAction.USER\_PROVIDED](../../com.aspose.words/resourceloadingaction/\#USER-PROVIDED).

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
| Daten | byte[] |  |

### setUri(String value) {#setUri-java.lang.String}
```
public void setUri(String value)
```


URI der Ressource, die zum Herunterladen verwendet wird, wenn [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) zurückgibt [ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction/\#DEFAULT).

Anfangs ist sie auf die absolute URI der Ressource gesetzt, aber der Benutzer kann sie auf einen beliebigen Wert neu definieren.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

