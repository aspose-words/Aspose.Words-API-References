---
title: BuiltInDocumentProperties
second_title: Aspose.Words for Java API 参考
description: 内置文档属性的集合。
type: docs
weight: 46
url: /zh/java/com.aspose.words/builtindocumentproperties/
---

**遗产：**
java.lang.Object, [com.aspose.words.DocumentPropertyCollection](../../com.aspose.words/documentpropertycollection)
```
public class BuiltInDocumentProperties extends DocumentPropertyCollection
```

内置文档属性的集合。

要了解更多信息，请访问**Work with Document Properties**文档文章。

提供访问[DocumentProperty](../../com.aspose.words/documentproperty)对象的名称（使用索引器）和一组类型化的属性，这些属性返回适当类型的值。

属性名称不区分大小写。

集合中的属性按名称的字母顺序排序。
## 方法

| 方法 | 描述 |
| --- | --- |
| [clear()](#clear--) | 从集合中删除所有属性。 |
| [contains(String name)](#contains-java.lang.String-) | 如果集合中存在具有指定名称的属性，则返回 true。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 返回一个[DocumentProperty](../../com.aspose.words/documentproperty)按索引的对象。 |
| [get(String name)](#get-java.lang.String-) | 返回一个[DocumentProperty](../../com.aspose.words/documentproperty)目的。 |
| [getAuthor()](#getAuthor--) | 获取文档作者的姓名。 |
| [getBytes()](#getBytes--) | 表示文档中字节数的估计值。 |
| [getCategory()](#getCategory--) | 获取文档的类别。 |
| [getCharacters()](#getCharacters--) | 表示文档中字符数的估计值。 |
| [getCharactersWithSpaces()](#getCharactersWithSpaces--) | 表示文档中字符数（包括空格）的估计值。 |
| [getClass()](#getClass--) |  |
| [getComments()](#getComments--) | 获取文档评论。 |
| [getCompany()](#getCompany--) | 获得公司财产。 |
| [getContentStatus()](#getContentStatus--) | 获取文档的 ContentStatus。 |
| [getContentType()](#getContentType--) | 获取文档的 ContentStatus。 |
| [getCount()](#getCount--) | 获取集合中的项目数。 |
| [getCreatedTime()](#getCreatedTime--) | 获取 UTC 文档创建日期。 |
| [getHeadingPairs()](#getHeadingPairs--) | 指定文档标题及其名称。 |
| [getHyperlinkBase()](#getHyperlinkBase--) | 指定用于评估本文档中的相关超链接的基本字符串。 |
| [getKeywords()](#getKeywords--) | 获取文档关键字。 |
| [getLastPrinted()](#getLastPrinted--) | 获取上次以 UTC 格式打印文档的日期。 |
| [getLastSavedBy()](#getLastSavedBy--) | 获取最后一位作者的姓名。 |
| [getLastSavedTime()](#getLastSavedTime--) | 获取上次保存的 UTC 时间。 |
| [getLines()](#getLines--) | 表示文档中行数的估计值。 |
| [getLinksUpToDate()](#getLinksUpToDate--) | 指示文档中的超链接是否是最新的。 |
| [getManager()](#getManager--) | 获取管理器属性。 |
| [getNameOfApplication()](#getNameOfApplication--) | 获取应用程序的名称。 |
| [getPages()](#getPages--) | 表示文档中页数的估计值。 |
| [getParagraphs()](#getParagraphs--) | 表示对文档中段落数的估计。 |
| [getRevisionNumber()](#getRevisionNumber--) | 获取文档修订号。 |
| [getSecurity()](#getSecurity--) | 将文档的安全级别指定为数值。 |
| [getSubject()](#getSubject--) | 获取文档的主题。 |
| [getTemplate()](#getTemplate--) | 获取文档模板的信息名称。 |
| [getThumbnail()](#getThumbnail--) | 获取或设置文档的缩略图。 |
| [getTitle()](#getTitle--) | 获取文档的标题。 |
| [getTitlesOfParts()](#getTitlesOfParts--) | 数组中的每个字符串指定文档中某个部分的名称。 |
| [getTotalEditingTime()](#getTotalEditingTime--) | 获取以分钟为单位的总编辑时间。 |
| [getVersion()](#getVersion--) | 表示创建文档的应用程序的版本号。 |
| [getWords()](#getWords--) | 表示对文档中字数的估计。 |
| [hashCode()](#hashCode--) |  |
| [indexOf(String name)](#indexOf-java.lang.String-) | 按名称获取属性的索引。 |
| [iterator()](#iterator--) | 返回一个迭代器对象，该对象可用于迭代集合中的所有项目。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(String name)](#remove-java.lang.String-) | 从集合中移除具有指定名称的属性。 |
| [removeAt(int index)](#removeAt-int-) | 删除指定索引处的属性。 |
| [setAuthor(String value)](#setAuthor-java.lang.String-) | 设置文档作者的姓名。 |
| [setBytes(int value)](#setBytes-int-) | 表示文档中字节数的估计值。 |
| [setCategory(String value)](#setCategory-java.lang.String-) | 设置文档的类别。 |
| [setCharacters(int value)](#setCharacters-int-) | 表示文档中字符数的估计值。 |
| [setCharactersWithSpaces(int value)](#setCharactersWithSpaces-int-) | 表示文档中字符数（包括空格）的估计值。 |
| [setComments(String value)](#setComments-java.lang.String-) | 设置文档注释。 |
| [setCompany(String value)](#setCompany-java.lang.String-) | 设置公司属性。 |
| [setContentStatus(String value)](#setContentStatus-java.lang.String-) | 设置文档的 ContentStatus。 |
| [setContentType(String value)](#setContentType-java.lang.String-) | 设置文档的 ContentStatus。 |
| [setCreatedTime(Date value)](#setCreatedTime-java.util.Date-) | 以 UTC 设置文档创建日期。 |
| [setHeadingPairs(Object[] value)](#setHeadingPairs-java.lang.Object---) | 指定文档标题及其名称。 |
| [setHyperlinkBase(String value)](#setHyperlinkBase-java.lang.String-) | 指定用于评估本文档中的相关超链接的基本字符串。 |
| [setKeywords(String value)](#setKeywords-java.lang.String-) | 设置文档关键字。 |
| [setLastPrinted(Date value)](#setLastPrinted-java.util.Date-) | 设置文档最后一次打印的日期，采用 UTC。 |
| [setLastSavedBy(String value)](#setLastSavedBy-java.lang.String-) | 设置最后一位作者的姓名。 |
| [setLastSavedTime(Date value)](#setLastSavedTime-java.util.Date-) | 以 UTC 设置上次保存的时间。 |
| [setLines(int value)](#setLines-int-) | 表示文档中行数的估计值。 |
| [setLinksUpToDate(boolean value)](#setLinksUpToDate-boolean-) | 指示文档中的超链接是否是最新的。 |
| [setManager(String value)](#setManager-java.lang.String-) | 设置管理器属性。 |
| [setNameOfApplication(String value)](#setNameOfApplication-java.lang.String-) | 设置应用程序的名称。 |
| [setPages(int value)](#setPages-int-) | 表示文档中页数的估计值。 |
| [setParagraphs(int value)](#setParagraphs-int-) | 表示对文档中段落数的估计。 |
| [setRevisionNumber(int value)](#setRevisionNumber-int-) | 设置文档修订号。 |
| [setSecurity(int value)](#setSecurity-int-) | 将文档的安全级别指定为数值。 |
| [setSubject(String value)](#setSubject-java.lang.String-) | 设置文档的主题。 |
| [setTemplate(String value)](#setTemplate-java.lang.String-) | 设置文档模板的信息名称。 |
| [setThumbnail(byte[] value)](#setThumbnail-byte---) | 获取或设置文档的缩略图。 |
| [setTitle(String value)](#setTitle-java.lang.String-) | 设置文档的标题。 |
| [setTitlesOfParts(String[] value)](#setTitlesOfParts-java.lang.String---) | 数组中的每个字符串指定文档中某个部分的名称。 |
| [setTotalEditingTime(int value)](#setTotalEditingTime-int-) | 以分钟为单位设置总编辑时间。 |
| [setVersion(int value)](#setVersion-int-) | 表示创建文档的应用程序的版本号。 |
| [setWords(int value)](#setWords-int-) | 表示对文档中字数的估计。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clear() {#clear--}
```
public void clear()
```


从集合中删除所有属性。

### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


如果集合中存在具有指定名称的属性，则返回 true。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 不区分大小写的属性名称。 |

**退货：**
boolean - 如果属性存在于集合中，则为真；否则为假。
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### get(int index) {#get-int-}
```
public DocumentProperty get(int index)
```


返回一个[DocumentProperty](../../com.aspose.words/documentproperty)按索引的对象。

**Note:**在 Java 中，这种方法很慢，因为它会遍历所有节点。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 的从零开始的索引[DocumentProperty](../../com.aspose.words/documentproperty)检索。 |

**退货：**
[DocumentProperty](../../com.aspose.words/documentproperty) - 一个[DocumentProperty](../../com.aspose.words/documentproperty)按索引的对象。
### get(String name) {#get-java.lang.String-}
```
public DocumentProperty get(String name)
```


返回一个[DocumentProperty](../../com.aspose.words/documentproperty)目的。返回一个[DocumentProperty](../../com.aspose.words/documentproperty)对象的属性名称。

属性的字符串名称对应于可用的类型化属性的名称[BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties).

如果您请求文档中不存在的属性，但该属性的名称被识别为有效的内置名称，则一个新的[DocumentProperty](../../com.aspose.words/documentproperty)创建、添加到集合并返回。新创建的属性被分配一个默认值（空字符串、零、假或 DateTime.MinValue，具体取决于内置属性的类型）。

如果您请求文档中不存在的属性并且该名称未被识别为内置名称，则返回 null。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 要检索的属性的不区分大小写的名称。 |

**退货：**
[DocumentProperty](../../com.aspose.words/documentproperty) - 相应的[DocumentProperty](../../com.aspose.words/documentproperty)价值。
### getAuthor() {#getAuthor--}
```
public String getAuthor()
```


获取文档作者的姓名。

**退货：**
java.lang.String - 文档作者的姓名。
### getBytes() {#getBytes--}
```
public int getBytes()
```


表示文档中字节数的估计值。

Microsoft Word 并不总是设置此属性。

Aspose.Words 不更新这个属性。

**退货：**
int - 相应的 int 值。
### getCategory() {#getCategory--}
```
public String getCategory()
```


获取文档的类别。

**退货：**
java.lang.String - 文档的类别。
### getCharacters() {#getCharacters--}
```
public int getCharacters()
```


表示文档中字符数的估计值。

 Aspose.Words 在您调用时更新此属性[Document.updateWordCount()](../../com.aspose.words/document\#updateWordCount--).

**退货：**
int - 相应的 int 值。
### getCharactersWithSpaces() {#getCharactersWithSpaces--}
```
public int getCharactersWithSpaces()
```


表示文档中字符数（包括空格）的估计值。

 Aspose.Words 在您调用时更新此属性[Document.updateWordCount()](../../com.aspose.words/document\#updateWordCount--).

**退货：**
int - 相应的 int 值。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getComments() {#getComments--}
```
public String getComments()
```


获取文档评论。

**退货：**
java.lang.String - 文档注释。
### getCompany() {#getCompany--}
```
public String getCompany()
```


获得公司财产。

**退货：**
java.lang.String - 公司财产。
### getContentStatus() {#getContentStatus--}
```
public String getContentStatus()
```


获取文档的 ContentStatus。

**退货：**
java.lang.String - 文档的 ContentStatus。
### getContentType() {#getContentType--}
```
public String getContentType()
```


获取文档的 ContentStatus。

**退货：**
java.lang.String - 文档的 ContentStatus。
### getCount() {#getCount--}
```
public int getCount()
```


获取集合中的项目数。

**退货：**
int - 集合中的项目数。
### getCreatedTime() {#getCreatedTime--}
```
public Date getCreatedTime()
```


获取 UTC 文档创建日期。

对于源自 RTF 格式的文档，此属性返回文档创建时作者机器的本地时间。

Aspose.Words 不更新这个属性。

**退货：**
java.util.Date - UTC 文档创建日期。
### getHeadingPairs() {#getHeadingPairs--}
```
public Object[] getHeadingPairs()
```


指定文档标题及其名称。

每个标题对占用此数组中的两个元素。

该对的第一个元素是 java.lang.String 并指定标题名称。该对的第二个元素是一个整数，它指定了该标题在[getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties\#getTitlesOfParts--) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties\#setTitlesOfParts-java.lang.String---)财产。

此属性中所有标题对的计数总和必须等于[getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties\#getTitlesOfParts--) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties\#setTitlesOfParts-java.lang.String---)财产。

Aspose.Words 不更新这个属性。

**退货：**
java.lang.Object[- 对应的java.lang.Object[] 价值。
### getHyperlinkBase() {#getHyperlinkBase--}
```
public String getHyperlinkBase()
```


指定用于评估本文档中的相关超链接的基本字符串。

Aspose.Words 不使用这个属性。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getKeywords() {#getKeywords--}
```
public String getKeywords()
```


获取文档关键字。

**退货：**
java.lang.String - 文档关键字。
### getLastPrinted() {#getLastPrinted--}
```
public Date getLastPrinted()
```


获取上次以 UTC 格式打印文档的日期。

对于源自 RTF 格式的文档，此属性返回上次打印操作的本地时间。

如果从未打印过文档，则此属性将返回 DateTime.MinValue。

Aspose.Words 不更新这个属性。

**退货：**
java.util.Date - 上次以 UTC 打印文档的日期。
### getLastSavedBy() {#getLastSavedBy--}
```
public String getLastSavedBy()
```


获取最后一位作者的姓名。

Aspose.Words 不更新这个属性。

**退货：**
java.lang.String - 最后一个作者的名字。
### getLastSavedTime() {#getLastSavedTime--}
```
public Date getLastSavedTime()
```


获取上次保存的 UTC 时间。

对于源自 RTF 格式的文档，此属性返回上次保存操作的本地时间。

Aspose.Words 不更新这个属性。

**退货：**
java.util.Date - 以 UTC 格式保存的最后时间。
### getLines() {#getLines--}
```
public int getLines()
```


表示文档中行数的估计值。

 Aspose.Words 在您调用时更新此属性[Document.updateWordCount(boolean)](../../com.aspose.words/document\#updateWordCount-boolean-).

**退货：**
int - 相应的 int 值。
### getLinksUpToDate() {#getLinksUpToDate--}
```
public boolean getLinksUpToDate()
```


指示文档中的超链接是否是最新的。

Aspose.Words 不更新这个属性。

**退货：**
boolean - 相应的布尔值。
### getManager() {#getManager--}
```
public String getManager()
```


获取管理器属性。

**退货：**
java.lang.String - 管理器属性。
### getNameOfApplication() {#getNameOfApplication--}
```
public String getNameOfApplication()
```


获取应用程序的名称。

**退货：**
java.lang.String - 应用程序的名称。
### getPages() {#getPages--}
```
public int getPages()
```


表示文档中页数的估计值。

 Aspose.Words 在您调用时更新此属性[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--).

**退货：**
int - 相应的 int 值。
### getParagraphs() {#getParagraphs--}
```
public int getParagraphs()
```


表示对文档中段落数的估计。

 Aspose.Words 在您调用时更新此属性[Document.updateWordCount()](../../com.aspose.words/document\#updateWordCount--).

**退货：**
int - 相应的 int 值。
### getRevisionNumber() {#getRevisionNumber--}
```
public int getRevisionNumber()
```


获取文档修订号。

Aspose.Words 不更新这个属性。

**退货：**
int - 文档修订号。
### getSecurity() {#getSecurity--}
```
public int getSecurity()
```


将文档的安全级别指定为数值。

将此属性仅用于提供信息，因为 Microsoft Word 并不总是设置此属性。此属性仅在 DOC 和 OOXML 文档中可用。

要保护或取消保护文档，请使用**M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)**和[Document.unprotect()](../../com.aspose.words/document\#unprotect--)方法。

Aspose.Words 在保存文档之前将此属性更新为正确的值。

**退货：**
 int - 相应的 int 值。返回值是按位组合[DocumentSecurity](../../com.aspose.words/documentsecurity)常数。
### getSubject() {#getSubject--}
```
public String getSubject()
```


获取文档的主题。

**退货：**
java.lang.String - 文档的主题。
### getTemplate() {#getTemplate--}
```
public String getTemplate()
```


获取文档模板的信息名称。

在 Microsoft Word 中，此属性仅供参考，通常仅包含模板的文件名，不包含路径。

空字符串表示文档附加到 Normal 模板。

要获取或设置附加模板的实际名称，请使用[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-)财产。

**退货：**
java.lang.String - 文档模板的信息名称。
### getThumbnail() {#getThumbnail--}
```
public byte[] getThumbnail()
```


获取或设置文档的缩略图。

目前此属性仅在将文档导出为 ePub 时使用，不会读取和写入其他文档格式。

可以将任意格式的图像设置为此属性，但在导出过程中会检查格式。如果图像无效或其格式不支持特定格式的文档，则抛出 java.lang.IllegalStateException。

只有 gif、jpeg 和 png 图像可用于 ePub 发布。

**退货：**
字节[- 对应的字节[] 价值。
### getTitle() {#getTitle--}
```
public String getTitle()
```


获取文档的标题。

**退货：**
java.lang.String - 文档的标题。
### getTitlesOfParts() {#getTitlesOfParts--}
```
public String[] getTitlesOfParts()
```


数组中的每个字符串指定文档中某个部分的名称。

Aspose.Words 不更新这个属性。

**退货：**
java.lang.字符串[] - 对应的java.lang.String[] 价值。
### getTotalEditingTime() {#getTotalEditingTime--}
```
public int getTotalEditingTime()
```


获取以分钟为单位的总编辑时间。

**退货：**
int - 以分钟为单位的总编辑时间。
### getVersion() {#getVersion--}
```
public int getVersion()
```


表示创建文档的应用程序的版本号。

当文档由 Microsoft Word 创建时，高 16 位代表主要版本，低 16 位代表内部版本号。

**退货：**
int - 相应的 int 值。
### getWords() {#getWords--}
```
public int getWords()
```


表示对文档中字数的估计。

 Aspose.Words 在您调用时更新此属性[Document.updateWordCount()](../../com.aspose.words/document\#updateWordCount--).

**退货：**
int - 相应的 int 值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### indexOf(String name) {#indexOf-java.lang.String-}
```
public int indexOf(String name)
```


按名称获取属性的索引。

**Note:**在 Java 中，这种方法很慢，因为它会遍历所有节点。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 不区分大小写的属性名称。 |

**退货：**
int - 从零开始的索引。如果未找到，则为负值。
### iterator() {#iterator--}
```
public Iterator iterator()
```


返回一个迭代器对象，该对象可用于迭代集合中的所有项目。

**退货：**
java.util.迭代器
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove(String name) {#remove-java.lang.String-}
```
public void remove(String name)
```


从集合中移除具有指定名称的属性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | java.lang.String | 不区分大小写的属性名称。 |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


删除指定索引处的属性。

**Note:**在 Java 中，这种方法很慢，因为它会遍历所有节点。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 从零开始的索引。 |

### setAuthor(String value) {#setAuthor-java.lang.String-}
```
public void setAuthor(String value)
```


设置文档作者的姓名。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 文档作者的姓名。 |

### setBytes(int value) {#setBytes-int-}
```
public void setBytes(int value)
```


表示文档中字节数的估计值。

Microsoft Word 并不总是设置此属性。

Aspose.Words 不更新这个属性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。 |

### setCategory(String value) {#setCategory-java.lang.String-}
```
public void setCategory(String value)
```


设置文档的类别。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 文档的类别。 |

### setCharacters(int value) {#setCharacters-int-}
```
public void setCharacters(int value)
```


表示文档中字符数的估计值。

 Aspose.Words 在您调用时更新此属性[Document.updateWordCount()](../../com.aspose.words/document\#updateWordCount--).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。 |

### setCharactersWithSpaces(int value) {#setCharactersWithSpaces-int-}
```
public void setCharactersWithSpaces(int value)
```


表示文档中字符数（包括空格）的估计值。

 Aspose.Words 在您调用时更新此属性[Document.updateWordCount()](../../com.aspose.words/document\#updateWordCount--).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。 |

### setComments(String value) {#setComments-java.lang.String-}
```
public void setComments(String value)
```


设置文档注释。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 文件评论。 |

### setCompany(String value) {#setCompany-java.lang.String-}
```
public void setCompany(String value)
```


设置公司属性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 公司财产。 |

### setContentStatus(String value) {#setContentStatus-java.lang.String-}
```
public void setContentStatus(String value)
```


设置文档的 ContentStatus。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 文档的 ContentStatus。 |

### setContentType(String value) {#setContentType-java.lang.String-}
```
public void setContentType(String value)
```


设置文档的 ContentStatus。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 文档的 ContentStatus。 |

### setCreatedTime(Date value) {#setCreatedTime-java.util.Date-}
```
public void setCreatedTime(Date value)
```


以 UTC 设置文档创建日期。

对于源自 RTF 格式的文档，此属性返回文档创建时作者机器的本地时间。

Aspose.Words 不更新这个属性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.Date | UTC 格式的文档创建日期。 |

### setHeadingPairs(Object[] value) {#setHeadingPairs-java.lang.Object---}
```
public void setHeadingPairs(Object[] value)
```


指定文档标题及其名称。

每个标题对占用此数组中的两个元素。

该对的第一个元素是 java.lang.String 并指定标题名称。该对的第二个元素是一个整数，它指定了该标题在[getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties\#getTitlesOfParts--) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties\#setTitlesOfParts-java.lang.String---)财产。

此属性中所有标题对的计数总和必须等于[getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties\#getTitlesOfParts--) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties\#setTitlesOfParts-java.lang.String---)财产。

Aspose.Words 不更新这个属性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.Object[] | 对应的 java.lang.Object[] 价值。 |

### setHyperlinkBase(String value) {#setHyperlinkBase-java.lang.String-}
```
public void setHyperlinkBase(String value)
```


指定用于评估本文档中的相关超链接的基本字符串。

Aspose.Words 不使用这个属性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setKeywords(String value) {#setKeywords-java.lang.String-}
```
public void setKeywords(String value)
```


设置文档关键字。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 文档关键字。 |

### setLastPrinted(Date value) {#setLastPrinted-java.util.Date-}
```
public void setLastPrinted(Date value)
```


设置文档最后一次打印的日期，采用 UTC。

对于源自 RTF 格式的文档，此属性返回上次打印操作的本地时间。

如果从未打印过文档，则此属性将返回 DateTime.MinValue。

Aspose.Words 不更新这个属性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.Date | 上次以 UTC 打印文档的日期。 |

### setLastSavedBy(String value) {#setLastSavedBy-java.lang.String-}
```
public void setLastSavedBy(String value)
```


设置最后一位作者的姓名。

Aspose.Words 不更新这个属性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 最后一位作者的姓名。 |

### setLastSavedTime(Date value) {#setLastSavedTime-java.util.Date-}
```
public void setLastSavedTime(Date value)
```


以 UTC 设置上次保存的时间。

对于源自 RTF 格式的文档，此属性返回上次保存操作的本地时间。

Aspose.Words 不更新这个属性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.util.Date | 最后一次保存的时间，以 UTC 表示。 |

### setLines(int value) {#setLines-int-}
```
public void setLines(int value)
```


表示文档中行数的估计值。

 Aspose.Words 在您调用时更新此属性[Document.updateWordCount(boolean)](../../com.aspose.words/document\#updateWordCount-boolean-).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。 |

### setLinksUpToDate(boolean value) {#setLinksUpToDate-boolean-}
```
public void setLinksUpToDate(boolean value)
```


指示文档中的超链接是否是最新的。

Aspose.Words 不更新这个属性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setManager(String value) {#setManager-java.lang.String-}
```
public void setManager(String value)
```


设置管理器属性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 经理财产。 |

### setNameOfApplication(String value) {#setNameOfApplication-java.lang.String-}
```
public void setNameOfApplication(String value)
```


设置应用程序的名称。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 应用程序的名称。 |

### setPages(int value) {#setPages-int-}
```
public void setPages(int value)
```


表示文档中页数的估计值。

 Aspose.Words 在您调用时更新此属性[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。 |

### setParagraphs(int value) {#setParagraphs-int-}
```
public void setParagraphs(int value)
```


表示对文档中段落数的估计。

 Aspose.Words 在您调用时更新此属性[Document.updateWordCount()](../../com.aspose.words/document\#updateWordCount--).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。 |

### setRevisionNumber(int value) {#setRevisionNumber-int-}
```
public void setRevisionNumber(int value)
```


设置文档修订号。

Aspose.Words 不更新这个属性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 文档修订号。 |

### setSecurity(int value) {#setSecurity-int-}
```
public void setSecurity(int value)
```


将文档的安全级别指定为数值。

将此属性仅用于提供信息，因为 Microsoft Word 并不总是设置此属性。此属性仅在 DOC 和 OOXML 文档中可用。

要保护或取消保护文档，请使用**M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)**和[Document.unprotect()](../../com.aspose.words/document\#unprotect--)方法。

Aspose.Words 在保存文档之前将此属性更新为正确的值。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是按位组合[DocumentSecurity](../../com.aspose.words/documentsecurity)常数。 |

### setSubject(String value) {#setSubject-java.lang.String-}
```
public void setSubject(String value)
```


设置文档的主题。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 文档的主题。 |

### setTemplate(String value) {#setTemplate-java.lang.String-}
```
public void setTemplate(String value)
```


设置文档模板的信息名称。

在 Microsoft Word 中，此属性仅供参考，通常仅包含模板的文件名，不包含路径。

空字符串表示文档附加到 Normal 模板。

要获取或设置附加模板的实际名称，请使用[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-)财产。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 文档模板的信息名称。 |

### setThumbnail(byte[] value) {#setThumbnail-byte---}
```
public void setThumbnail(byte[] value)
```


获取或设置文档的缩略图。

目前此属性仅在将文档导出为 ePub 时使用，不会读取和写入其他文档格式。

可以将任意格式的图像设置为此属性，但在导出过程中会检查格式。如果图像无效或其格式不支持特定格式的文档，则抛出 java.lang.IllegalStateException。

只有 gif、jpeg 和 png 图像可用于 ePub 发布。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | byte[] | 对应的字节[] 价值。 |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


设置文档的标题。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 文档的标题。 |

### setTitlesOfParts(String[] value) {#setTitlesOfParts-java.lang.String---}
```
public void setTitlesOfParts(String[] value)
```


数组中的每个字符串指定文档中某个部分的名称。

Aspose.Words 不更新这个属性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String[] | 对应的 java.lang.String[] 价值。 |

### setTotalEditingTime(int value) {#setTotalEditingTime-int-}
```
public void setTotalEditingTime(int value)
```


以分钟为单位设置总编辑时间。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 以分钟为单位的总编辑时间。 |

### setVersion(int value) {#setVersion-int-}
```
public void setVersion(int value)
```


表示创建文档的应用程序的版本号。

当文档由 Microsoft Word 创建时，高 16 位代表主要版本，低 16 位代表内部版本号。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。 |

### setWords(int value) {#setWords-int-}
```
public void setWords(int value)
```


表示对文档中字数的估计。

 Aspose.Words 在您调用时更新此属性[Document.updateWordCount()](../../com.aspose.words/document\#updateWordCount--).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。 |

### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
