---
title: "ResourceLoadingArgs"
linktitle: "ResourceLoadingArgs"
second_title: "Aspose.Words para Java"
description: "Proporciona datos para el método IResourceLoadingCallback.resourceLoadingcom.aspose.words.ResourceLoadingArgs en Java."
type: docs
weight: 576
url: /es/java/com.aspose.words/resourceloadingargs/
---

**Inheritance:**
java.lang.Object
```
public class ResourceLoadingArgs
```

Proporciona datos para el método [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs).

 **Examples:** 

Muestra cómo personalizar el proceso de carga de recursos externos en un documento.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getOriginalUri()](#getOriginalUri) | URI original del recurso según lo especificado en el documento importado. |
| [getResourceType()](#getResourceType) | Tipo de recurso. |
| [getUri()](#getUri) | URI del recurso que se utiliza para la descarga si [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) devuelve [ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction/\#DEFAULT). |
| [setData(byte[] data)](#setData-byte) | Establece los datos proporcionados por el usuario del recurso que se utilizan si [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) devuelve [ResourceLoadingAction.USER\_PROVIDED](../../com.aspose.words/resourceloadingaction/\#USER-PROVIDED). |
| [setUri(String value)](#setUri-java.lang.String) | URI del recurso que se utiliza para la descarga si [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) devuelve [ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction/\#DEFAULT). |
### getOriginalUri() {#getOriginalUri}
```
public String getOriginalUri()
```


URI original del recurso según lo especificado en el documento importado.

 **Examples:** 

Muestra cómo personalizar el proceso de carga de recursos externos en un documento.

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
java.lang.String - El valor java.lang.String correspondiente.
### getResourceType() {#getResourceType}
```
public int getResourceType()
```


Tipo de recurso.

 **Examples:** 

Muestra cómo personalizar el proceso de carga de recursos externos en un documento.

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
int - El valor entero correspondiente. El valor devuelto es una de las constantes de [ResourceType](../../com.aspose.words/resourcetype/).
### getUri() {#getUri}
```
public String getUri()
```


URI del recurso que se utiliza para la descarga si [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) devuelve [ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction/\#DEFAULT).

Inicialmente se establece en la URI absoluta del recurso, pero el usuario puede redefinirla a cualquier valor.

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### setData(byte[] data) {#setData-byte}
```
public void setData(byte[] data)
```


Establece los datos proporcionados por el usuario del recurso que se utilizan si [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) devuelve [ResourceLoadingAction.USER\_PROVIDED](../../com.aspose.words/resourceloadingaction/\#USER-PROVIDED).

 **Examples:** 

Muestra cómo personalizar el proceso de carga de recursos externos en un documento.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| datos | byte[] |  |

### setUri(String value) {#setUri-java.lang.String}
```
public void setUri(String value)
```


URI del recurso que se utiliza para la descarga si [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) devuelve [ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction/\#DEFAULT).

Inicialmente se establece en la URI absoluta del recurso, pero el usuario puede redefinirla a cualquier valor.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

