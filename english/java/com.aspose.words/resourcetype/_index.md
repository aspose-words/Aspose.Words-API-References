---
title: ResourceType
linktitle: ResourceType
second_title: Aspose.Words for Java
description: Type of loaded resource in Java.
type: docs
weight: 572
url: /java/com.aspose.words/resourcetype/
---

**Inheritance:**
java.lang.Object
```
public class ResourceType
```

Type of loaded resource.

 **Examples:** 

Shows how to customize the process of loading external resources into a document.

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
                 args.setData(DocumentHelper.getBytesFromStream(new URI("http://www.google.com/images/logos/ps_logo2.png").toURL().openStream()));

                 return ResourceLoadingAction.USER_PROVIDED;
             }

             if ("Aspose logo".equals(args.getOriginalUri())) {
                 args.setData(DocumentHelper.getBytesFromStream(getAsposelogoUri().toURL().openStream()));

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
## Fields

| Field | Description |
| --- | --- |
| [CSS_STYLE_SHEET](#CSS-STYLE-SHEET) | CSS style sheet. |
| [DOCUMENT](#DOCUMENT) | Document. |
| [FONT](#FONT) | Font. |
| [IMAGE](#IMAGE) | Image. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String resourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int resourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int resourceType)](#toString-int) |  |
### CSS_STYLE_SHEET {#CSS-STYLE-SHEET}
```
public static int CSS_STYLE_SHEET
```


CSS style sheet.

### DOCUMENT {#DOCUMENT}
```
public static int DOCUMENT
```


Document.

### FONT {#FONT}
```
public static int FONT
```


Font.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


Image.

### length {#length}
```
public static int length
```


### fromName(String resourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String resourceTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| resourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int resourceType) {#getName-int}
```
public static String getName(int resourceType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| resourceType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int resourceType) {#toString-int}
```
public static String toString(int resourceType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| resourceType | int |  |

**Returns:**
java.lang.String
