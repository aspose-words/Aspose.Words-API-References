---
title: "ResourceLoadingAction"
linktitle: "ResourceLoadingAction"
second_title: "Aspose.Words per Java"
description: "Specifica la modalità di caricamento delle risorse in Java."
type: docs
weight: 575
url: /it/java/com.aspose.words/resourceloadingaction/
---

**Inheritance:**
java.lang.Object
```
public class ResourceLoadingAction
```

Specifica la modalità di caricamento delle risorse.

Per saperne di più, visita l'articolo di documentazione [ Specify Load Options ][Specify Load Options].

 **Examples:** 

Mostra come personalizzare il processo di caricamento di risorse esterne in un documento.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [DEFAULT](#DEFAULT) | Aspose.Words caricherà questa risorsa come al solito. |
| [SKIP](#SKIP) | Aspose.Words salterà il caricamento di questa risorsa. |
| [USER_PROVIDED](#USER-PROVIDED) | Aspose.Words utilizzerà l'array di byte fornito dall'utente in [ResourceLoadingArgs.setData(byte[])](../../com.aspose.words/resourceloadingargs/\#setData-byte) come dati della risorsa. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String resourceLoadingActionName)](#fromName-java.lang.String) |  |
| [getName(int resourceLoadingAction)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int resourceLoadingAction)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Aspose.Words caricherà questa risorsa come al solito.

### SKIP {#SKIP}
```
public static int SKIP
```


Aspose.Words salterà il caricamento di questa risorsa. Verrà memorizzato solo il collegamento senza dati per un'immagine, il foglio di stile CSS sarà ignorato per il formato HTML.

### USER_PROVIDED {#USER-PROVIDED}
```
public static int USER_PROVIDED
```


Aspose.Words utilizzerà l'array di byte fornito dall'utente in [ResourceLoadingArgs.setData(byte[])](../../com.aspose.words/resourceloadingargs/\#setData-byte) come dati della risorsa.

### length {#length}
```
public static int length
```


### fromName(String resourceLoadingActionName) {#fromName-java.lang.String}
```
public static int fromName(String resourceLoadingActionName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| resourceLoadingActionName | java.lang.String |  |

**Returns:**
int
### getName(int resourceLoadingAction) {#getName-int}
```
public static String getName(int resourceLoadingAction)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| resourceLoadingAction | int |  |

**Returns:**
java.lang.String
