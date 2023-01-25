---
title: IFieldMergingCallback
second_title: Aspose.Words for Java API Reference
description: Implement this interface if you want to control how data is inserted into merge fields during a mail merge operation.
type: docs
weight: 645
url: /java/com.aspose.words/ifieldmergingcallback/
---
```
public interface IFieldMergingCallback
```

Implement this interface if you want to control how data is inserted into merge fields during a mail merge operation.
## Methods

| Method | Description |
| --- | --- |
| [fieldMerging(FieldMergingArgs args)](#fieldMerging-com.aspose.words.FieldMergingArgs) | Called when the Aspose.Words mail merge engine is about to insert data into a merge field in the document. |
| [imageFieldMerging(ImageFieldMergingArgs args)](#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs) | Called when the Aspose.Words mail merge engine is about to insert an image into a merge field. |
### fieldMerging(FieldMergingArgs args) {#fieldMerging-com.aspose.words.FieldMergingArgs}
```
public abstract void fieldMerging(FieldMergingArgs args)
```


Called when the Aspose.Words mail merge engine is about to insert data into a merge field in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| args | [FieldMergingArgs](../../com.aspose.words/fieldmergingargs) |  |

### imageFieldMerging(ImageFieldMergingArgs args) {#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs}
```
public abstract void imageFieldMerging(ImageFieldMergingArgs args)
```


Called when the Aspose.Words mail merge engine is about to insert an image into a merge field.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| args | [ImageFieldMergingArgs](../../com.aspose.words/imagefieldmergingargs) |  |

