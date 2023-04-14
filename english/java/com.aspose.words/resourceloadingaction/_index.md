---
title: ResourceLoadingAction
linktitle: ResourceLoadingAction
second_title: Aspose.Words for Java API Reference
description: Specifies the mode of resource loading in Java.
type: docs
weight: 488
url: /java/com.aspose.words/resourceloadingaction/
---

**Inheritance:**
java.lang.Object
```
public class ResourceLoadingAction
```

Specifies the mode of resource loading.

To learn more, visit the [ Specify Load Options ][Specify Load Options] documentation article.

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


[Specify Load Options]: https://docs.aspose.com/words/java/specify-load-options/
## Fields

| Field | Description |
| --- | --- |
| [DEFAULT](#DEFAULT) | Aspose.Words will load this resource as usual. |
| [SKIP](#SKIP) | Aspose.Words will skip loading of this resource. |
| [USER_PROVIDED](#USER-PROVIDED) | Aspose.Words will use byte array provided by user in [ResourceLoadingArgs.setData(byte[])](../../com.aspose.words/resourceloadingargs/\#setData-byte) as resource data. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String resourceLoadingActionName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int resourceLoadingAction)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int resourceLoadingAction)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Aspose.Words will load this resource as usual.

### SKIP {#SKIP}
```
public static int SKIP
```


Aspose.Words will skip loading of this resource. Only link without data will be stored for an image, CSS style sheet will be ignored for HTML format.

### USER_PROVIDED {#USER-PROVIDED}
```
public static int USER_PROVIDED
```


Aspose.Words will use byte array provided by user in [ResourceLoadingArgs.setData(byte[])](../../com.aspose.words/resourceloadingargs/\#setData-byte) as resource data.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fromName(String resourceLoadingActionName) {#fromName-java.lang.String}
```
public static int fromName(String resourceLoadingActionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| resourceLoadingActionName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int resourceLoadingAction) {#getName-int}
```
public static String getName(int resourceLoadingAction)
```




**Parameters:**
| Parameter | Type | Description |
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
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(int resourceLoadingAction) {#toString-int}
```
public static String toString(int resourceLoadingAction)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| resourceLoadingAction | int |  |

**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

