---
title: Range
second_title: Aspose.Words for Java API 参考
description: 表示文档中的一个连续区域。
type: docs
weight: 472
url: /zh/java/com.aspose.words/range/
---

**遗产：**
java.lang.Object
```
public class Range
```

表示文档中的一个连续区域。

要了解更多信息，请访问**Working with Ranges**文档文章。

文档由节点树表示，节点提供操作树的操作，但如果将文档视为连续的文本序列，则某些操作更容易执行。

**Range**是一个“外观”接口，它提供将文档或文档的一部分视为“平面”文本的方法，而不管文档节点存储在树状对象模型中的事实。

**Range**不包含任何文本或节点，它只是文档片段上的视图或“窗口”。
## 方法

| 方法 | 描述 |
| --- | --- |
| [delete()](#delete--) | 删除范围内的所有字符。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarks()](#getBookmarks--) | 返回一个[getBookmarks()](../../com.aspose.words/range\#getBookmarks--)代表范围内所有书签的集合。 |
| [getClass()](#getClass--) |  |
| [getFields()](#getFields--) | 返回一个[getFields()](../../com.aspose.words/range\#getFields--)表示范围内所有字段的集合。 |
| [getFormFields()](#getFormFields--) | 返回一个[getFormFields()](../../com.aspose.words/range\#getFormFields--)表示范围内所有表单字段的集合。 |
| [getStructuredDocumentTags()](#getStructuredDocumentTags--) | 返回一个[getStructuredDocumentTags()](../../com.aspose.words/range\#getStructuredDocumentTags--)表示范围内所有结构化文档标签的集合。 |
| [getText()](#getText--) | 获取范围的文本。 |
| [hashCode()](#hashCode--) |  |
| [normalizeFieldTypes()](#normalizeFieldTypes--) | 更改字段类型值[FieldChar.getFieldType()](../../com.aspose.words/fieldchar\#getFieldType--)的[FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend)在此范围内，以便它们对应于字段代码中包含的字段类型。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [replace(String pattern, String replacement)](#replace-java.lang.String-java.lang.String-) | 用替换字符串替换所有出现的指定字符串模式。 |
| [replace(String pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions-) | 用替换字符串替换所有出现的指定字符串模式。 |
| [replace(Pattern pattern, String replacement)](#replace-java.util.regex.Pattern-java.lang.String-) | 用另一个字符串替换由正则表达式指定的字符模式的所有匹配项。 |
| [replace(Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions-) | 用另一个字符串替换由正则表达式指定的字符模式的所有匹配项。 |
| [toDocument()](#toDocument--) | 构造一个包含范围的新的完全形成的文档。 |
| [toString()](#toString--) |  |
| [unlinkFields()](#unlinkFields--) | 取消链接此范围内的字段。 |
| [updateFields()](#updateFields--) | 更新此范围内文档字段的值。 |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### delete() {#delete--}
```
public void delete()
```


删除范围内的所有字符。

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
### getBookmarks() {#getBookmarks--}
```
public BookmarkCollection getBookmarks()
```


返回一个[getBookmarks()](../../com.aspose.words/range\#getBookmarks--)代表范围内所有书签的集合。

**退货：**
[BookmarkCollection](../../com.aspose.words/bookmarkcollection) - 一个[getBookmarks()](../../com.aspose.words/range\#getBookmarks--)代表范围内所有书签的集合。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getFields() {#getFields--}
```
public FieldCollection getFields()
```


返回一个[getFields()](../../com.aspose.words/range\#getFields--)表示范围内所有字段的集合。

**退货：**
[FieldCollection](../../com.aspose.words/fieldcollection) - 一个[getFields()](../../com.aspose.words/range\#getFields--)表示范围内所有字段的集合。
### getFormFields() {#getFormFields--}
```
public FormFieldCollection getFormFields()
```


返回一个[getFormFields()](../../com.aspose.words/range\#getFormFields--)表示范围内所有表单字段的集合。

**退货：**
[FormFieldCollection](../../com.aspose.words/formfieldcollection) - 一个[getFormFields()](../../com.aspose.words/range\#getFormFields--)表示范围内所有表单字段的集合。
### getStructuredDocumentTags() {#getStructuredDocumentTags--}
```
public StructuredDocumentTagCollection getStructuredDocumentTags()
```


返回一个[getStructuredDocumentTags()](../../com.aspose.words/range\#getStructuredDocumentTags--)表示范围内所有结构化文档标签的集合。

**退货：**
[StructuredDocumentTagCollection](../../com.aspose.words/structureddocumenttagcollection) - 一个[getStructuredDocumentTags()](../../com.aspose.words/range\#getStructuredDocumentTags--)表示范围内所有结构化文档标签的集合。
### getText() {#getText--}
```
public String getText()
```


获取范围的文本。

返回的字符串包括所有控制字符和特殊字符，如[ControlChar](../../com.aspose.words/controlchar).

**退货：**
java.lang.String - 范围的文本。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### normalizeFieldTypes() {#normalizeFieldTypes--}
```
public void normalizeFieldTypes()
```


更改字段类型值[FieldChar.getFieldType()](../../com.aspose.words/fieldchar\#getFieldType--)的[FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend)在此范围内，以便它们对应于字段代码中包含的字段类型。

在影响字段类型的文档更改后使用此方法。

要更改整个文档中的字段类型值，请使用[Document.normalizeFieldTypes()](../../com.aspose.words/document\#normalizeFieldTypes--).

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### replace(String pattern, String replacement) {#replace-java.lang.String-java.lang.String-}
```
public int replace(String pattern, String replacement)
```


用替换字符串替换所有出现的指定字符串模式。

该模式不会用作正则表达式。请用[replace(java.util.regex.Pattern, java.lang.String)](../../com.aspose.words/range\#replace-java.util.regex.Pattern--java.lang.String-)如果你需要正则表达式。

使用不区分大小写的比较。

方法能够处理模式和替换字符串中的中断。

如果你需要使用中断，你应该使用特殊的元字符：

 *  **&p** \- 段落中断
 *  **&b** \分节符
 *  **&m** \分页符
 *  **&l** \手动换行

使用方法[replace(java.lang.String, java.lang.String, com.aspose.words.FindReplaceOptions)](../../com.aspose.words/range\#replace-java.lang.String--java.lang.String--com.aspose.words.FindReplaceOptions-)进行更灵活的定制。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pattern | java.lang.String | 要替换的字符串。 |
| replacement | java.lang.String | 替换所有出现的模式的字符串。 |

**退货：**
int - 进行的替换次数。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.Writeln("Numbers 1, 2, 3");

 // Inserts paragraph break after Numbers.
 doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
 
```
### replace(String pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions-}
```
public int replace(String pattern, String replacement, FindReplaceOptions options)
```


用替换字符串替换所有出现的指定字符串模式。

该模式不会用作正则表达式。请用[replace(java.util.regex.Pattern, java.lang.String, com.aspose.words.FindReplaceOptions)](../../com.aspose.words/range\#replace-java.util.regex.Pattern--java.lang.String--com.aspose.words.FindReplaceOptions-)如果你需要正则表达式。

方法能够处理模式和替换字符串中的中断。

如果你需要使用中断，你应该使用特殊的元字符：

 *  **&p** \- 段落中断
 *  **&b** \分节符
 *  **&m** \分页符
 *  **&l** \手动换行
 *  **&&** \- ＆ 特点

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pattern | java.lang.String | 要替换的字符串。 |
| replacement | java.lang.String | 替换所有出现的模式的字符串。 |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions) | \{[FindReplaceOptions](../../com.aspose.words/findreplaceoptions)对象以指定其他选项。 |

**退货：**
int - 进行的替换次数。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.Writeln("Numbers 1, 2, 3");

 // Inserts paragraph break after Numbers.
 doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
 
```
### replace(Pattern pattern, String replacement) {#replace-java.util.regex.Pattern-java.lang.String-}
```
public int replace(Pattern pattern, String replacement)
```


用另一个字符串替换由正则表达式指定的字符模式的所有匹配项。

替换正则表达式捕获的整个匹配项。

方法能够处理模式和替换字符串中的中断。

如果你需要使用中断，你应该使用特殊的元字符：

 *  **&p** \- 段落中断
 *  **&b** \分节符
 *  **&m** \分页符
 *  **&l** \手动换行

使用方法[replace(java.util.regex.Pattern, java.lang.String, com.aspose.words.FindReplaceOptions)](../../com.aspose.words/range\#replace-java.util.regex.Pattern--java.lang.String--com.aspose.words.FindReplaceOptions-)进行更灵活的定制。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pattern | java.util.regex.Pattern | 用于查找匹配项的正则表达式模式。 |
| replacement | java.lang.String | 替换所有出现的模式的字符串。 |

**退货：**
int - 进行的替换次数。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.Writeln("a1, b2, c3");

 // Replaces each number with paragraph break.
 doc.Range.Replace(new Regex(@"\d+"), "&p");
 
```
### replace(Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions-}
```
public int replace(Pattern pattern, String replacement, FindReplaceOptions options)
```


用另一个字符串替换由正则表达式指定的字符模式的所有匹配项。

替换正则表达式捕获的整个匹配项。

方法能够处理模式和替换字符串中的中断。

如果你需要使用中断，你应该使用特殊的元字符：

 *  **&p** \- 段落中断
 *  **&b** \分节符
 *  **&m** \分页符
 *  **&l** \手动换行
 *  **&&** \- ＆ 特点

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pattern | java.util.regex.Pattern | 用于查找匹配项的正则表达式模式。 |
| replacement | java.lang.String | 替换所有出现的模式的字符串。 |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions) | \{[FindReplaceOptions](../../com.aspose.words/findreplaceoptions)对象以指定其他选项。 |

**退货：**
int - 进行的替换次数。

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.Writeln("a1, b2, c3");

 // Replaces each number with paragraph break.
 doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
 
```
### toDocument() {#toDocument--}
```
public Document toDocument()
```


构造一个包含范围的新的完全形成的文档。

**退货：**
[Document](../../com.aspose.words/document)
### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### unlinkFields() {#unlinkFields--}
```
public void unlinkFields()
```


取消链接此范围内的字段。

将此范围内的所有字段替换为其最近的结果。

要取消链接整个文档中的字段，请使用[unlinkFields()](../../com.aspose.words/range\#unlinkFields--).

### updateFields() {#updateFields--}
```
public void updateFields()
```


更新此范围内文档字段的值。

当您打开、修改然后保存文档时，Aspose.Words 不会自动更新字段，而是保持它们的完整性。因此，如果您以编程方式修改了文档并希望确保正确的（计算的）字段值出现在保存的文档中，则通常需要在保存之前调用此方法。

执行邮件合并后不需要更新字段，因为邮件合并是一种字段更新，会自动更新文档中的所有字段。

此方法不会更新所有字段类型。有关支持的字段类型的详细列表，请参阅《程序员指南》。

此方法不会更新与页面布局算法相关的字段（例如 PAGE、PAGES、PAGEREF）。当您呈现文档或调用时，页面布局相关的字段会更新[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--).

要更新整个文档中的字段，请使用[Document.updateFields()](../../com.aspose.words/document\#updateFields--).

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
