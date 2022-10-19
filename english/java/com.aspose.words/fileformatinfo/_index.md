---
title: FileFormatInfo
second_title: Aspose.Words for Java API Reference
description: Contains data returned by  document format detection methods.
type: docs
weight: 265
url: /java/com.aspose.words/fileformatinfo/
---

**Inheritance:**
java.lang.Object
```
public class FileFormatInfo
```

Contains data returned by [FileFormatUtil](../../com.aspose.words/fileformatutil) document format detection methods.

To learn more, visit the **Detect File Format and Check Format Compatibility** documentation article.

You do not create instances of this class directly. Objects of this class are returned by **M:Aspose.Words.FileFormatUtil.DetectFileFormat(System.IO.Stream)** methods.
## Methods

| Method | Description |
| --- | --- |
| [getLoadFormat()](#getLoadFormat--) | Gets the detected document format. |
| [isEncrypted()](#isEncrypted--) | Returns true if the document is encrypted and requires a password to open. |
| [hasDigitalSignature()](#hasDigitalSignature--) | Returns true if this document contains a digital signature. |
| [getEncoding()](#getEncoding--) | Gets the detected encoding if applicable to the current document format. |
### getLoadFormat() {#getLoadFormat--}
```
public int getLoadFormat()
```


Gets the detected document format.

When an OOXML document is encrypted, it is not possible to ascertained whether it is an Excel, Word or PowerPoint document without decrypting it first so for an encrypted OOXML document this property will always return [LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX).

**Returns:**
int - The detected document format. The returned value is one of [LoadFormat](../../com.aspose.words/loadformat) constants.
### isEncrypted() {#isEncrypted--}
```
public boolean isEncrypted()
```


Returns true if the document is encrypted and requires a password to open.

This property exists to help you sort documents that are encrypted from those that are not. If you attempt to load an encrypted document using Aspose.Words without supplying a password an exception will be thrown. You can use this property to detect whether a document requires a password and take some action before loading a document, for example, prompt the user for a password.

**Returns:**
boolean - True if the document is encrypted and requires a password to open.
### hasDigitalSignature() {#hasDigitalSignature--}
```
public boolean hasDigitalSignature()
```


Returns true if this document contains a digital signature. This property merely informs that a digital signature is present on a document, but it does not specify whether the signature is valid or not.

This property exists to help you sort documents that are digitally signed from those that are not. If you use Aspose.Words to modify and save a document that is digitally signed, then the digital signature will be lost. This is by design because a digital signature exists to guard the authenticity of a document. Using this property you can detect digitally signed documents before processing them in the same way as normal documents and take some action to avoid losing the digital signature, for example notify the user.

**Returns:**
boolean - True if this document contains a digital signature.
### getEncoding() {#getEncoding--}
```
public Charset getEncoding()
```


Gets the detected encoding if applicable to the current document format. At the moment detects encoding only for HTML documents.

**Returns:**
java.nio.charset.Charset - The detected encoding if applicable to the current document format.
