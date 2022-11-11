---
title: FileFormatUtil
second_title: Aspose.Words for Java API Reference
description: 提供用于处理文件格式的实用方法，例如检测文件格式或将文件扩展名转换为/从文件格式枚举。
type: docs
weight: 266
url: /zh/java/com.aspose.words/fileformatutil/
---

**遗产:**
java.lang.Object
```
public class FileFormatUtil
```

提供用于处理文件格式的实用方法，例如检测文件格式或将文件扩展名转换为/从文件格式枚举。

要了解更多信息，请访问**Detect File Format and Check Format Compatibility**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [content类型ToLoadFormat(String content类型)](#content类型ToLoadFormat-java.lang.String-) | 将 IANA 内容类型转换为加载格式枚举值。 |
| [content类型ToSaveFormat(String content类型)](#content类型ToSaveFormat-java.lang.String-) | 将 IANA 内容类型转换为保存格式枚举值。 |
| [detectFileFormat(InputStream stream)](#detectFileFormat-java.io.InputStream-) |  |
| [detectFileFormat(String fileName)](#detectFileFormat-java.lang.String-) | 检测并返回有关文档格式的信息。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [extensionToSaveFormat(String extension)](#extensionToSaveFormat-java.lang.String-) | 将文件扩展名转换为[SaveFormat](../../com.aspose.words/saveformat)价值。 |
| [get班级()](#get班级--) |  |
| [hashCode()](#hashCode--) |  |
| [image类型ToExtension(int image类型)](#image类型ToExtension-int-) |  |
| [loadFormatToExtension(int loadFormat)](#loadFormatToExtension-int-) |  |
| [loadFormatToSaveFormat(int loadFormat)](#loadFormatToSaveFormat-int-) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [saveFormatToExtension(int saveFormat)](#saveFormatToExtension-int-) |  |
| [saveFormatToLoadFormat(int saveFormat)](#saveFormatToLoadFormat-int-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### content类型ToLoadFormat(String content类型) {#content类型ToLoadFormat-java.lang.String-}
```
public static int content类型ToLoadFormat(String content类型)
```


将 IANA 内容类型转换为加载格式枚举值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| content类型 | java.lang.String |  |

**退货:**
整数
### content类型ToSaveFormat(String content类型) {#content类型ToSaveFormat-java.lang.String-}
```
public static int content类型ToSaveFormat(String content类型)
```


将 IANA 内容类型转换为保存格式枚举值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| content类型 | java.lang.String |  |

**退货:**
整数
### detectFileFormat(InputStream stream) {#detectFileFormat-java.io.InputStream-}
```
public static FileFormatInfo detectFileFormat(InputStream stream)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**退货:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo)
### detectFileFormat(String fileName) {#detectFileFormat-java.lang.String-}
```
public static FileFormatInfo detectFileFormat(String fileName)
```


检测并返回有关文档格式的信息。检测并返回有关存储在磁盘文件中的文档格式的信息。

即使该方法检测到文档格式，也不能保证指定的文档是有效的。该方法仅通过读取足以检测的数据来检测文档格式。要完全验证文档是否有效，您需要将文档加载到[Document](../../com.aspose.words/document)目的。

这个方法抛出[FileCorruptedException](../../com.aspose.words/filecorruptedexception)当格式被识别，但由于损坏而无法完成检测。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 文件名。 |

**退货:**
[FileFormatInfo](../../com.aspose.words/fileformatinfo) - 一个[FileFormatInfo](../../com.aspose.words/fileformatinfo)包含检测到的信息的对象。
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
### extensionToSaveFormat(String extension) {#extensionToSaveFormat-java.lang.String-}
```
public static int extensionToSaveFormat(String extension)
```


将文件扩展名转换为[SaveFormat](../../com.aspose.words/saveformat)价值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| extension | java.lang.String | 文件扩展名。可以带或不带前导点。不区分大小写。

如果无法识别扩展名，则返回[SaveFormat.UNKNOWN](../../com.aspose.words/saveformat\#UNKNOWN). |

**退货:**
整数
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
### image类型ToExtension(int image类型) {#image类型ToExtension-int-}
```
public static String image类型ToExtension(int image类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| image类型 | int |  |

**退货:**
java.lang.String
### loadFormatToExtension(int loadFormat) {#loadFormatToExtension-int-}
```
public static String loadFormatToExtension(int loadFormat)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| loadFormat | int |  |

**退货:**
java.lang.String
### loadFormatToSaveFormat(int loadFormat) {#loadFormatToSaveFormat-int-}
```
public static int loadFormatToSaveFormat(int loadFormat)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| loadFormat | int |  |

**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### saveFormatToExtension(int saveFormat) {#saveFormatToExtension-int-}
```
public static String saveFormatToExtension(int saveFormat)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | int |  |

**退货:**
java.lang.String
### saveFormatToLoadFormat(int saveFormat) {#saveFormatToLoadFormat-int-}
```
public static int saveFormatToLoadFormat(int saveFormat)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | int |  |

**退货:**
整数
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
