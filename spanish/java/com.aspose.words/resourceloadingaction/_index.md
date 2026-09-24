---
title: "ResourceLoadingAction"
linktitle: "ResourceLoadingAction"
second_title: "Aspose.Words para Java"
description: "Especifica el modo de carga de recursos en Java."
type: docs
weight: 575
url: /es/java/com.aspose.words/resourceloadingaction/
---

**Inheritance:**
java.lang.Object
```
public class ResourceLoadingAction
```

Especifica el modo de carga de recursos.

Para obtener más información, visite el artículo de documentación [ Specify Load Options ][Specify Load Options].

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


[Specify Load Options]: https://docs.aspose.com/words/java/specify-load-options/
## Campos

| Campo | Descripción |
| --- | --- |
| [DEFAULT](#DEFAULT) | Aspose.Words cargará este recurso como de costumbre. |
| [SKIP](#SKIP) | Aspose.Words omitirá la carga de este recurso. |
| [USER_PROVIDED](#USER-PROVIDED) | Aspose.Words utilizará la matriz de bytes proporcionada por el usuario en [ResourceLoadingArgs.setData(byte[])](../../com.aspose.words/resourceloadingargs/\#setData-byte) como datos del recurso. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String resourceLoadingActionName)](#fromName-java.lang.String) |  |
| [getName(int resourceLoadingAction)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int resourceLoadingAction)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Aspose.Words cargará este recurso como de costumbre.

### SKIP {#SKIP}
```
public static int SKIP
```


Aspose.Words omitirá la carga de este recurso. Sólo se almacenará el enlace sin datos para una imagen, la hoja de estilo CSS será ignorada para el formato HTML.

### USER_PROVIDED {#USER-PROVIDED}
```
public static int USER_PROVIDED
```


Aspose.Words utilizará la matriz de bytes proporcionada por el usuario en [ResourceLoadingArgs.setData(byte[])](../../com.aspose.words/resourceloadingargs/\#setData-byte) como datos del recurso.

### length {#length}
```
public static int length
```


### fromName(String resourceLoadingActionName) {#fromName-java.lang.String}
```
public static int fromName(String resourceLoadingActionName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| resourceLoadingActionName | java.lang.String |  |

**Returns:**
int
### getName(int resourceLoadingAction) {#getName-int}
```
public static String getName(int resourceLoadingAction)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| resourceLoadingAction | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int resourceLoadingAction) {#toString-int}
```
public static String toString(int resourceLoadingAction)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| resourceLoadingAction | int |  |

**Returns:**
java.lang.String
