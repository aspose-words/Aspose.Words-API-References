---
title: "ResourceLoadingArgs"
linktitle: "ResourceLoadingArgs"
second_title: "Aspose.Words لـ Java"
description: "يوفر البيانات لطريقة IResourceLoadingCallback.resourceLoadingcom.aspose.words.ResourceLoadingArgs في Java."
type: docs
weight: 576
url: /ar/java/com.aspose.words/resourceloadingargs/
---

**Inheritance:**
java.lang.Object
```
public class ResourceLoadingArgs
```

يوفر البيانات لطريقة [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs).

 **Examples:** 

يوضح كيفية تخصيص عملية تحميل الموارد الخارجية إلى مستند.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getOriginalUri()](#getOriginalUri) | URI الأصلي للمورد كما هو محدد في المستند المستورد. |
| [getResourceType()](#getResourceType) | نوع المورد. |
| [getUri()](#getUri) | URI للمورد الذي يُستخدم للتنزيل إذا كانت طريقة [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) تُعيد [ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction/\#DEFAULT). |
| [setData(byte[] data)](#setData-byte) | يضبط البيانات التي يقدمها المستخدم للمورد والتي تُستخدم إذا كانت طريقة [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) تُعيد [ResourceLoadingAction.USER\_PROVIDED](../../com.aspose.words/resourceloadingaction/\#USER-PROVIDED). |
| [setUri(String value)](#setUri-java.lang.String) | URI للمورد الذي يُستخدم للتنزيل إذا كانت طريقة [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) تُعيد [ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction/\#DEFAULT). |
### getOriginalUri() {#getOriginalUri}
```
public String getOriginalUri()
```


URI الأصلي للمورد كما هو محدد في المستند المستورد.

 **Examples:** 

يوضح كيفية تخصيص عملية تحميل الموارد الخارجية إلى مستند.

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
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getResourceType() {#getResourceType}
```
public int getResourceType()
```


نوع المورد.

 **Examples:** 

يوضح كيفية تخصيص عملية تحميل الموارد الخارجية إلى مستند.

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
int - قيمة int المقابلة. القيمة المرجعة هي واحدة من ثوابت [ResourceType](../../com.aspose.words/resourcetype/).
### getUri() {#getUri}
```
public String getUri()
```


URI للمورد الذي يُستخدم للتنزيل إذا كانت طريقة [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) تُعيد [ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction/\#DEFAULT).

في البداية يتم تعيينه إلى URI مطلق للمورد، لكن يمكن للمستخدم إعادة تعريفه إلى أي قيمة.

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### setData(byte[] data) {#setData-byte}
```
public void setData(byte[] data)
```


يضبط البيانات التي يقدمها المستخدم للمورد والتي تُستخدم إذا كانت طريقة [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) تُعيد [ResourceLoadingAction.USER\_PROVIDED](../../com.aspose.words/resourceloadingaction/\#USER-PROVIDED).

 **Examples:** 

يوضح كيفية تخصيص عملية تحميل الموارد الخارجية إلى مستند.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| بيانات | byte[] |  |

### setUri(String value) {#setUri-java.lang.String}
```
public void setUri(String value)
```


URI للمورد الذي يُستخدم للتنزيل إذا كانت طريقة [IResourceLoadingCallback.resourceLoading(com.aspose.words.ResourceLoadingArgs)](../../com.aspose.words/iresourceloadingcallback/\#resourceLoading-com.aspose.words.ResourceLoadingArgs) تُعيد [ResourceLoadingAction.DEFAULT](../../com.aspose.words/resourceloadingaction/\#DEFAULT).

في البداية يتم تعيينه إلى URI مطلق للمورد، لكن يمكن للمستخدم إعادة تعريفه إلى أي قيمة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

