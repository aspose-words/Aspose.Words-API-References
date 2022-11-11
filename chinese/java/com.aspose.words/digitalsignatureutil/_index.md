---
title: DigitalSignatureUtil
second_title: Aspose.Words for Java API Reference
description: 提供签署文件的方法。
type: docs
weight: 114
url: /zh/java/com.aspose.words/digitalsignatureutil/
---

**遗产:**
java.lang.Object
```
public class DigitalSignatureUtil
```

提供签署文件的方法。

要了解更多信息，请访问**Work with Digital Signatures**文档文章。

由于数字签名适用于文件内容而不是文档对象模型，因此这些方法被放入一个单独的类中。

支持的格式是[LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC)和[LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX).
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [hashCode()](#hashCode--) |  |
| [loadSignatures(InputStream stream)](#loadSignatures-java.io.InputStream-) |  |
| [loadSignatures(String fileName)](#loadSignatures-java.lang.String-) | 从文档加载数字签名。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeAllSignatures(InputStream srcStream, OutputStream dstStream)](#removeAllSignatures-java.io.InputStream-java.io.OutputStream-) |  |
| [removeAllSignatures(String srcFileName, String dstFileName)](#removeAllSignatures-java.lang.String-java.lang.String-) | 从源文件中删除所有数字签名并将未签名的文件写入目标文件。 |
| [sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder)](#sign-java.io.InputStream-java.io.OutputStream-com.aspose.words.CertificateHolder-) |  |
| [sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder, SignOptions signOptions)](#sign-java.io.InputStream-java.io.OutputStream-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions-) |  |
| [sign(String srcFileName, String dstFileName, CertificateHolder certHolder)](#sign-java.lang.String-java.lang.String-com.aspose.words.CertificateHolder-) | 使用给定的标志源文档[CertificateHolder](../../com.aspose.words/certificateholder)带有数字签名并将签名的文档写入目标文件。 |
| [sign(String srcFileName, String dstFileName, CertificateHolder certHolder, SignOptions signOptions)](#sign-java.lang.String-java.lang.String-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions-) | 使用给定的标志源文档[CertificateHolder](../../com.aspose.words/certificateholder)和[SignOptions](../../com.aspose.words/signoptions)带有数字签名并将签名的文档写入目标文件。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### loadSignatures(InputStream stream) {#loadSignatures-java.io.InputStream-}
```
public static DigitalSignatureCollection loadSignatures(InputStream stream)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**退货:**
[DigitalSignatureCollection](../../com.aspose.words/digitalsignaturecollection)
### loadSignatures(String fileName) {#loadSignatures-java.lang.String-}
```
public static DigitalSignatureCollection loadSignatures(String fileName)
```


从文档加载数字签名。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 文档的路径。 |

**退货:**
[DigitalSignatureCollection](../../com.aspose.words/digitalsignaturecollection) - 收集数字签名。如果文件未签名，则返回空集合。
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### removeAllSignatures(InputStream srcStream, OutputStream dstStream) {#removeAllSignatures-java.io.InputStream-java.io.OutputStream-}
```
public static void removeAllSignatures(InputStream srcStream, OutputStream dstStream)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcStream | java.io.InputStream |  |
| dstStream | java.io.OutputStream |  |

### removeAllSignatures(String srcFileName, String dstFileName) {#removeAllSignatures-java.lang.String-java.lang.String-}
```
public static void removeAllSignatures(String srcFileName, String dstFileName)
```


从源文件中删除所有数字签名并将未签名的文件写入目标文件。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcFileName | java.lang.String |  |
| dstFileName | java.lang.String |  |

### sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder) {#sign-java.io.InputStream-java.io.OutputStream-com.aspose.words.CertificateHolder-}
```
public static void sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcStream | java.io.InputStream |  |
| dstStream | java.io.OutputStream |  |
| certHolder | [CertificateHolder](../../com.aspose.words/certificateholder) |  |

### sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder, SignOptions signOptions) {#sign-java.io.InputStream-java.io.OutputStream-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions-}
```
public static void sign(InputStream srcStream, OutputStream dstStream, CertificateHolder certHolder, SignOptions signOptions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcStream | java.io.InputStream |  |
| dstStream | java.io.OutputStream |  |
| certHolder | [CertificateHolder](../../com.aspose.words/certificateholder) |  |
| signOptions | [SignOptions](../../com.aspose.words/signoptions) |  |

### sign(String srcFileName, String dstFileName, CertificateHolder certHolder) {#sign-java.lang.String-java.lang.String-com.aspose.words.CertificateHolder-}
```
public static void sign(String srcFileName, String dstFileName, CertificateHolder certHolder)
```


使用给定的标志源文档[CertificateHolder](../../com.aspose.words/certificateholder)带有数字签名并将签名的文档写入目标文件。

文件应该是[LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC)或者[LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcFileName | java.lang.String | 要签名的文档的文件名。 |
| dstFileName | java.lang.String | 签名文档输出的文件名。 |
| certHolder | [CertificateHolder](../../com.aspose.words/certificateholder) | \{[CertificateHolder](../../com.aspose.words/certificateholder)带有用于签署文件的证书的对象。 |

### sign(String srcFileName, String dstFileName, CertificateHolder certHolder, SignOptions signOptions) {#sign-java.lang.String-java.lang.String-com.aspose.words.CertificateHolder-com.aspose.words.SignOptions-}
```
public static void sign(String srcFileName, String dstFileName, CertificateHolder certHolder, SignOptions signOptions)
```


使用给定的标志源文档[CertificateHolder](../../com.aspose.words/certificateholder)和[SignOptions](../../com.aspose.words/signoptions)带有数字签名并将签名的文档写入目标文件。

文件应该是[LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC)或者[LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcFileName | java.lang.String | 要签名的文档的文件名。 |
| dstFileName | java.lang.String | 签名文档输出的文件名。 |
| certHolder | [CertificateHolder](../../com.aspose.words/certificateholder) | \{[CertificateHolder](../../com.aspose.words/certificateholder)带有用于签署文件的证书的对象。 |
| signOptions | [SignOptions](../../com.aspose.words/signoptions) | \{[SignOptions](../../com.aspose.words/signoptions)具有各种签名选项的对象。 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
