---
title: DigitalSignatureUtil
second_title: Aspose.Words for Java API Reference
description: Provides methods for signing document.
type: docs
weight: 114
url: /java/com.aspose.words/digitalsignatureutil/
---

**Inheritance:**
java.lang.Object
```
public class DigitalSignatureUtil
```

Provides methods for signing document.

To learn more, visit the **Work with Digital Signatures** documentation article.

Since digital signature works with file content rather than Document Object Model these methods are put into a separate class.

Supported formats are [LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC) and [LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX).
## Methods

| Method | Description |
| --- | --- |
| [sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder, SignOptions signOptions)](#sign-java.io.InputStream-java.io.OutputStream-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions-) |  |
| [sign(String srcFileName, String dstFileName, CertificateHolder certHolder, SignOptions signOptions)](#sign-java.lang.String-java.lang.String-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions-) | Signs source document using given [CertificateHolder](../../com.aspose.words/certificateholder) and [SignOptions](../../com.aspose.words/signoptions) with digital signature and writes signed document to destination file. |
| [sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder)](#sign-java.io.InputStream-java.io.OutputStream-com.aspose.words.CertificateHolder-) |  |
| [sign(String srcFileName, String dstFileName, CertificateHolder certHolder)](#sign-java.lang.String-java.lang.String-com.aspose.words.CertificateHolder-) | Signs source document using given [CertificateHolder](../../com.aspose.words/certificateholder) with digital signature and writes signed document to destination file. |
| [removeAllSignatures(String srcFileName, String dstFileName)](#removeAllSignatures-java.lang.String-java.lang.String-) | Removes all digital signatures from source file and writes unsigned file to destination file. |
| [removeAllSignatures(InputStream srcStream, OutputStream dstStream)](#removeAllSignatures-java.io.InputStream-java.io.OutputStream-) |  |
| [loadSignatures(String fileName)](#loadSignatures-java.lang.String-) | Loads digital signatures from document. |
| [loadSignatures(InputStream stream)](#loadSignatures-java.io.InputStream-) |  |
### sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder, SignOptions signOptions) {#sign-java.io.InputStream-java.io.OutputStream-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions-}
```
public static void sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder, SignOptions signOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | java.io.InputStream |  |
| dstStream | java.io.OutputStream |  |
| certHolder | [CertificateHolder](../../com.aspose.words/certificateholder) |  |
| signOptions | [SignOptions](../../com.aspose.words/signoptions) |  |

### sign(String srcFileName, String dstFileName, CertificateHolder certHolder, SignOptions signOptions) {#sign-java.lang.String-java.lang.String-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions-}
```
public static void sign(String srcFileName, String dstFileName, CertificateHolder certHolder, SignOptions signOptions)
```


Signs source document using given [CertificateHolder](../../com.aspose.words/certificateholder) and [SignOptions](../../com.aspose.words/signoptions) with digital signature and writes signed document to destination file.

Document should be either [LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC) or [LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcFileName | java.lang.String | The file name of the document to sign. |
| dstFileName | java.lang.String | The file name of the signed document output. |
| certHolder | [CertificateHolder](../../com.aspose.words/certificateholder) | \{[CertificateHolder](../../com.aspose.words/certificateholder) object with certificate that used to sign file. |
| signOptions | [SignOptions](../../com.aspose.words/signoptions) | \{[SignOptions](../../com.aspose.words/signoptions) object with various signing options. |

### sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder) {#sign-java.io.InputStream-java.io.OutputStream-com.aspose.words.CertificateHolder-}
```
public static void sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | java.io.InputStream |  |
| dstStream | java.io.OutputStream |  |
| certHolder | [CertificateHolder](../../com.aspose.words/certificateholder) |  |

### sign(String srcFileName, String dstFileName, CertificateHolder certHolder) {#sign-java.lang.String-java.lang.String-com.aspose.words.CertificateHolder-}
```
public static void sign(String srcFileName, String dstFileName, CertificateHolder certHolder)
```


Signs source document using given [CertificateHolder](../../com.aspose.words/certificateholder) with digital signature and writes signed document to destination file.

Document should be either [LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC) or [LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcFileName | java.lang.String | The file name of the document to sign. |
| dstFileName | java.lang.String | The file name of the signed document output. |
| certHolder | [CertificateHolder](../../com.aspose.words/certificateholder) | \{[CertificateHolder](../../com.aspose.words/certificateholder) object with certificate that used to sign file. |

### removeAllSignatures(String srcFileName, String dstFileName) {#removeAllSignatures-java.lang.String-java.lang.String-}
```
public static void removeAllSignatures(String srcFileName, String dstFileName)
```


Removes all digital signatures from source file and writes unsigned file to destination file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcFileName | java.lang.String |  |
| dstFileName | java.lang.String |  |

### removeAllSignatures(InputStream srcStream, OutputStream dstStream) {#removeAllSignatures-java.io.InputStream-java.io.OutputStream-}
```
public static void removeAllSignatures(InputStream srcStream, OutputStream dstStream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| srcStream | java.io.InputStream |  |
| dstStream | java.io.OutputStream |  |

### loadSignatures(String fileName) {#loadSignatures-java.lang.String-}
```
public static DigitalSignatureCollection loadSignatures(String fileName)
```


Loads digital signatures from document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | Path to the document. |

**Returns:**
[DigitalSignatureCollection](../../com.aspose.words/digitalsignaturecollection) - Collection of digital signatures. Returns empty collection if file is not signed.
### loadSignatures(InputStream stream) {#loadSignatures-java.io.InputStream-}
```
public static DigitalSignatureCollection loadSignatures(InputStream stream)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Returns:**
[DigitalSignatureCollection](../../com.aspose.words/digitalsignaturecollection)