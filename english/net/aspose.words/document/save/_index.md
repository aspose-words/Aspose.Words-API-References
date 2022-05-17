---
title: Save
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 680
url: /net/aspose.words/document/save/
---
## Document.Save method (1 of 6)

Saves the document to a file. Automatically determines the save format from the extension.

```csharp
public SaveOutputParameters Save(string fileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |

## Return Value

Additional information that you can optionally use.

### See Also

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

---

## Document.Save method (2 of 6)

Saves the document to a file in the specified format.

```csharp
public SaveOutputParameters Save(string fileName, SaveFormat saveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |
| saveFormat | SaveFormat | The format in which to save the document. |

## Return Value

Additional information that you can optionally use.

### See Also

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters)
* enum [SaveFormat](../../saveformat)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

---

## Document.Save method (3 of 6)

Saves the document to a file using the specified save options.

```csharp
public SaveOutputParameters Save(string fileName, SaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The name for the document. If a document with the specified file name already exists, the existing document is overwritten. |
| saveOptions | SaveOptions | Specifies the options that control how the document is saved. Can be null. |

## Return Value

Additional information that you can optionally use.

### See Also

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters)
* class [SaveOptions](../../../aspose.words.saving/saveoptions)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

---

## Document.Save method (4 of 6)

Saves the document to a stream using the specified format.

```csharp
public SaveOutputParameters Save(Stream stream, SaveFormat saveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | Stream where to save the document. |
| saveFormat | SaveFormat | The format in which to save the document. |

## Return Value

Additional information that you can optionally use.

### See Also

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters)
* enum [SaveFormat](../../saveformat)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

---

## Document.Save method (5 of 6)

Saves the document to a stream using the specified save options.

```csharp
public SaveOutputParameters Save(Stream stream, SaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | Stream where to save the document. |
| saveOptions | SaveOptions | Specifies the options that control how the document is saved. Can be null. If this is null, the document will be saved in the binary DOC format. |

## Return Value

Additional information that you can optionally use.

### See Also

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters)
* class [SaveOptions](../../../aspose.words.saving/saveoptions)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

---

## Document.Save method (6 of 6)

Sends the document to the client browser.

```csharp
public SaveOutputParameters Save(HttpResponse response, string fileName, 
    ContentDisposition contentDisposition, SaveOptions saveOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| response | HttpResponse | Response object where to save the document. |
| fileName | String | The name for the document that will appear at the client browser. The name should not contain path. |
| contentDisposition | ContentDisposition | A [`ContentDisposition`](../../contentdisposition) value that specifies how the document is presented at the client browser. |
| saveOptions | SaveOptions | Specifies the options that control how the document is saved. Can be null. |

## Return Value

Additional information that you can optionally use.

### Remarks

Internally, this method saves to a memory stream first and then copies to the response stream because the response stream does not support seek.

### See Also

* class [SaveOutputParameters](../../../aspose.words.saving/saveoutputparameters)
* enum [ContentDisposition](../../contentdisposition)
* class [SaveOptions](../../../aspose.words.saving/saveoptions)
* class [Document](../../document)
* namespace [Aspose.Words](../../document)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
