---
title: FindReplaceOptions
second_title: Aspose.Words for Java API 参考
description: 指定查找/替换操作的选项。
type: docs
weight: 270
url: /zh/java/com.aspose.words/findreplaceoptions/
---

**遗产：**
java.lang.Object
```
public class FindReplaceOptions
```

指定查找/替换操作的选项。

要了解更多信息，请访问**Find and Replace**文档文章。
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [FindReplaceOptions()](#FindReplaceOptions--) | 初始化此类的新实例。 |
| [FindReplaceOptions(int direction)](#FindReplaceOptions-int-) | 初始化此类的新实例。 |
| [FindReplaceOptions(IReplacingCallback replacingCallback)](#FindReplaceOptions-com.aspose.words.IReplacingCallback-) | 初始化此类的新实例。 |
| [FindReplaceOptions(int direction, IReplacingCallback replacingCallback)](#FindReplaceOptions-int-com.aspose.words.IReplacingCallback-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getApplyFont()](#getApplyFont--) | 应用于新内容的文本格式。 |
| [getApplyParagraphFormat()](#getApplyParagraphFormat--) | 应用于新内容的段落格式。 |
| [getClass()](#getClass--) |  |
| [getDirection()](#getDirection--) | 选择替换方向。 |
| [getFindWholeWordsOnly()](#getFindWholeWordsOnly--) | True 表示 oldValue 必须是一个独立的词。 |
| [getIgnoreDeleted()](#getIgnoreDeleted--) | 获取一个布尔值，指示忽略删除修订中的文本。 |
| [getIgnoreFieldCodes()](#getIgnoreFieldCodes--) | 获取一个布尔值，指示忽略域代码中的文本。 |
| [getIgnoreFields()](#getIgnoreFields--) | 获取一个布尔值，指示忽略字段内的文本。 |
| [getIgnoreFootnotes()](#getIgnoreFootnotes--) | 获取一个布尔值，指示忽略脚注。 |
| [getIgnoreInserted()](#getIgnoreInserted--) | 获取一个布尔值，指示忽略插入修订中的文本。 |
| [getIgnoreStructuredDocumentTags()](#getIgnoreStructuredDocumentTags--) | 获取一个布尔值，指示忽略内容[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag). |
| [getLegacyMode()](#getLegacyMode--) | 获取一个布尔值，指示使用旧的查找/替换算法。 |
| [getMatchCase()](#getMatchCase--) | True 表示区分大小写比较，false 表示不区分大小写比较。 |
| [getReplacingCallback()](#getReplacingCallback--) | 在每次替换发生之前调用的用户定义方法。 |
| [getSmartParagraphBreakReplacement()](#getSmartParagraphBreakReplacement--) | 获取或设置一个布尔值，指示是否允许在没有下一个同级段落时替换分段符。 |
| [getUseLegacyOrder()](#getUseLegacyOrder--) | True 表示考虑文本框从上到下按顺序执行文本搜索。 |
| [getUseSubstitutions()](#getUseSubstitutions--) | 获取一个布尔值，指示是否识别和使用替换模式中的替换。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setDirection(int value)](#setDirection-int-) | 选择替换方向。 |
| [setFindWholeWordsOnly(boolean value)](#setFindWholeWordsOnly-boolean-) | True 表示 oldValue 必须是一个独立的词。 |
| [setIgnoreDeleted(boolean value)](#setIgnoreDeleted-boolean-) | 设置一个布尔值，指示忽略删除修订中的文本。 |
| [setIgnoreFieldCodes(boolean value)](#setIgnoreFieldCodes-boolean-) | 设置一个布尔值，指示忽略字段代码中的文本。 |
| [setIgnoreFields(boolean value)](#setIgnoreFields-boolean-) | 设置一个布尔值，指示忽略字段内的文本。 |
| [setIgnoreFootnotes(boolean value)](#setIgnoreFootnotes-boolean-) | 设置一个布尔值，指示忽略脚注。 |
| [setIgnoreInserted(boolean value)](#setIgnoreInserted-boolean-) | 设置一个布尔值，指示忽略插入修订中的文本。 |
| [setIgnoreStructuredDocumentTags(boolean value)](#setIgnoreStructuredDocumentTags-boolean-) | 设置一个布尔值，指示要么忽略[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag). |
| [setLegacyMode(boolean value)](#setLegacyMode-boolean-) | 设置一个布尔值，指示使用旧的查找/替换算法。 |
| [setMatchCase(boolean value)](#setMatchCase-boolean-) | True 表示区分大小写比较，false 表示不区分大小写比较。 |
| [setReplacingCallback(IReplacingCallback value)](#setReplacingCallback-com.aspose.words.IReplacingCallback-) | 在每次替换发生之前调用的用户定义方法。 |
| [setSmartParagraphBreakReplacement(boolean value)](#setSmartParagraphBreakReplacement-boolean-) | 获取或设置一个布尔值，指示是否允许在没有下一个同级段落时替换分段符。 |
| [setUseLegacyOrder(boolean value)](#setUseLegacyOrder-boolean-) | True 表示考虑文本框从上到下按顺序执行文本搜索。 |
| [setUseSubstitutions(boolean value)](#setUseSubstitutions-boolean-) | 设置一个布尔值，指示是否识别和使用替换模式中的替换。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FindReplaceOptions() {#FindReplaceOptions--}
```
public FindReplaceOptions()
```


初始化此类的新实例。

### FindReplaceOptions(int direction) {#FindReplaceOptions-int-}
```
public FindReplaceOptions(int direction)
```


初始化此类的新实例。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| direction | int |  |

### FindReplaceOptions(IReplacingCallback replacingCallback) {#FindReplaceOptions-com.aspose.words.IReplacingCallback-}
```
public FindReplaceOptions(IReplacingCallback replacingCallback)
```


初始化此类的新实例。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback) |  |

### FindReplaceOptions(int direction, IReplacingCallback replacingCallback) {#FindReplaceOptions-int-com.aspose.words.IReplacingCallback-}
```
public FindReplaceOptions(int direction, IReplacingCallback replacingCallback)
```


初始化此类的新实例。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| direction | int |  |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback) |  |

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
### getApplyFont() {#getApplyFont--}
```
public Font getApplyFont()
```


应用于新内容的文本格式。

**退货：**
[Font](../../com.aspose.words/font) - 相应的[Font](../../com.aspose.words/font)价值。
### getApplyParagraphFormat() {#getApplyParagraphFormat--}
```
public ParagraphFormat getApplyParagraphFormat()
```


应用于新内容的段落格式。

**退货：**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - 相应的[ParagraphFormat](../../com.aspose.words/paragraphformat)价值。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getDirection() {#getDirection--}
```
public int getDirection()
```


选择替换方向。默认值为[FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection\#FORWARD).

**退货：**
int - 相应的 int 值。返回值是其中之一[FindReplaceDirection](../../com.aspose.words/findreplacedirection)常数。
### getFindWholeWordsOnly() {#getFindWholeWordsOnly--}
```
public boolean getFindWholeWordsOnly()
```


True 表示 oldValue 必须是一个独立的词。

**退货：**
boolean - 相应的布尔值。
### getIgnoreDeleted() {#getIgnoreDeleted--}
```
public boolean getIgnoreDeleted()
```


获取一个布尔值，指示忽略删除修订中的文本。默认值为 false 。

**退货：**
boolean - 一个布尔值，指示忽略删除修订中的文本。
### getIgnoreFieldCodes() {#getIgnoreFieldCodes--}
```
public boolean getIgnoreFieldCodes()
```


获取一个布尔值，指示忽略域代码中的文本。默认值为 false 。

此选项仅影响域代码（它不会忽略[NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype\#FIELD-SEPARATOR)和[NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END)）。

要忽略整个字段，请使用相应的选项[getIgnoreFields()](../../com.aspose.words/findreplaceoptions\#getIgnoreFields--) / [setIgnoreFields(boolean)](../../com.aspose.words/findreplaceoptions\#setIgnoreFields-boolean-).

**退货：**
boolean - 一个布尔值，指示忽略域代码内的文本。
### getIgnoreFields() {#getIgnoreFields--}
```
public boolean getIgnoreFields()
```


获取一个布尔值，指示忽略字段内的文本。默认值为 false 。

此选项影响整个字段（之间的所有节点[NodeType.FIELD\_START](../../com.aspose.words/nodetype\#FIELD-START)和[NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END)）。

要仅忽略域代码，请使用相应的选项[getIgnoreFieldCodes()](../../com.aspose.words/findreplaceoptions\#getIgnoreFieldCodes--) / [setIgnoreFieldCodes(boolean)](../../com.aspose.words/findreplaceoptions\#setIgnoreFieldCodes-boolean-).

**退货：**
boolean - 一个布尔值，指示忽略字段内的文本。
### getIgnoreFootnotes() {#getIgnoreFootnotes--}
```
public boolean getIgnoreFootnotes()
```


获取一个布尔值，指示忽略脚注。默认值为 false 。

**退货：**
boolean - 一个布尔值，指示忽略脚注。
### getIgnoreInserted() {#getIgnoreInserted--}
```
public boolean getIgnoreInserted()
```


获取一个布尔值，指示忽略插入修订中的文本。默认值为 false 。

**退货：**
boolean - 一个布尔值，指示忽略插入修订中的文本。
### getIgnoreStructuredDocumentTags() {#getIgnoreStructuredDocumentTags--}
```
public boolean getIgnoreStructuredDocumentTags()
```


获取一个布尔值，指示忽略内容[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag).默认值为 false 。

当此选项设置为 true 时，内容[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)将被视为简单文本。

否则，[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)将作为独立故事处理，替换模式将分别搜索每个[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) 所以如果模式穿过[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)，则不会对这种模式进行替换。

**退货：**
 boolean - 一个布尔值，指示忽略内容[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag).
### getLegacyMode() {#getLegacyMode--}
```
public boolean getLegacyMode()
```


获取一个布尔值，指示使用旧的查找/替换算法。如果您需要与引入高级查找/替换功能之前完全相同的行为，请使用此标志。请注意，旧算法不支持高级功能，例如替换为中断、应用格式等。

**退货：**
boolean - 一个布尔值，表示使用旧的查找/替换算法。
### getMatchCase() {#getMatchCase--}
```
public boolean getMatchCase()
```


True 表示区分大小写比较，false 表示不区分大小写比较。

**退货：**
boolean - 相应的布尔值。
### getReplacingCallback() {#getReplacingCallback--}
```
public IReplacingCallback getReplacingCallback()
```


在每次替换发生之前调用的用户定义方法。

**退货：**
[IReplacingCallback](../../com.aspose.words/ireplacingcallback) - 相应的[IReplacingCallback](../../com.aspose.words/ireplacingcallback)价值。
### getSmartParagraphBreakReplacement() {#getSmartParagraphBreakReplacement--}
```
public boolean getSmartParagraphBreakReplacement()
```


获取或设置一个布尔值，指示是否允许在没有下一个同级段落时替换分段符。

默认值为 false 。

当没有下一个所有子节点都可以移动到的同级段落时，此选项允许通过在被替换的段落之后找到任何（不一定是同级）下一段来替换分段符。

**退货：**
boolean - 相应的布尔值。
### getUseLegacyOrder() {#getUseLegacyOrder--}
```
public boolean getUseLegacyOrder()
```


True 表示考虑文本框从上到下按顺序执行文本搜索。默认值为假。

**退货：**
boolean - 相应的布尔值。
### getUseSubstitutions() {#getUseSubstitutions--}
```
public boolean getUseSubstitutions()
```


获取一个布尔值，指示是否识别和使用替换模式中的替换。默认值为 false 。有关替换元素的详细信息，请参阅：https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions。

**退货：**
boolean - 一个布尔值，指示是否识别和使用替换模式中的替换。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setDirection(int value) {#setDirection-int-}
```
public void setDirection(int value)
```


选择替换方向。默认值为[FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection\#FORWARD).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[FindReplaceDirection](../../com.aspose.words/findreplacedirection)常数。 |

### setFindWholeWordsOnly(boolean value) {#setFindWholeWordsOnly-boolean-}
```
public void setFindWholeWordsOnly(boolean value)
```


True 表示 oldValue 必须是一个独立的词。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setIgnoreDeleted(boolean value) {#setIgnoreDeleted-boolean-}
```
public void setIgnoreDeleted(boolean value)
```


设置一个布尔值，指示忽略删除修订中的文本。默认值为 false 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示忽略删除修订中的文本。 |

### setIgnoreFieldCodes(boolean value) {#setIgnoreFieldCodes-boolean-}
```
public void setIgnoreFieldCodes(boolean value)
```


设置一个布尔值，指示忽略字段代码中的文本。默认值为 false 。

此选项仅影响域代码（它不会忽略[NodeType.FIELD\_SEPARATOR](../../com.aspose.words/nodetype\#FIELD-SEPARATOR)和[NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END)）。

要忽略整个字段，请使用相应的选项[getIgnoreFields()](../../com.aspose.words/findreplaceoptions\#getIgnoreFields--) / [setIgnoreFields(boolean)](../../com.aspose.words/findreplaceoptions\#setIgnoreFields-boolean-).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示忽略字段代码中的文本。 |

### setIgnoreFields(boolean value) {#setIgnoreFields-boolean-}
```
public void setIgnoreFields(boolean value)
```


设置一个布尔值，指示忽略字段内的文本。默认值为 false 。

此选项影响整个字段（之间的所有节点[NodeType.FIELD\_START](../../com.aspose.words/nodetype\#FIELD-START)和[NodeType.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END)）。

要仅忽略域代码，请使用相应的选项[getIgnoreFieldCodes()](../../com.aspose.words/findreplaceoptions\#getIgnoreFieldCodes--) / [setIgnoreFieldCodes(boolean)](../../com.aspose.words/findreplaceoptions\#setIgnoreFieldCodes-boolean-).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示忽略字段内的文本。 |

### setIgnoreFootnotes(boolean value) {#setIgnoreFootnotes-boolean-}
```
public void setIgnoreFootnotes(boolean value)
```


设置一个布尔值，指示忽略脚注。默认值为 false 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示忽略脚注。 |

### setIgnoreInserted(boolean value) {#setIgnoreInserted-boolean-}
```
public void setIgnoreInserted(boolean value)
```


设置一个布尔值，指示忽略插入修订中的文本。默认值为 false 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示忽略插入修订中的文本。 |

### setIgnoreStructuredDocumentTags(boolean value) {#setIgnoreStructuredDocumentTags-boolean-}
```
public void setIgnoreStructuredDocumentTags(boolean value)
```


设置一个布尔值，指示要么忽略[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag).默认值为 false 。

当此选项设置为 true 时，内容[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)将被视为简单文本。

否则，[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)将作为独立故事处理，替换模式将分别搜索每个[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) 所以如果模式穿过[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)，则不会对这种模式进行替换。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示忽略内容[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag). |

### setLegacyMode(boolean value) {#setLegacyMode-boolean-}
```
public void setLegacyMode(boolean value)
```


设置一个布尔值，指示使用旧的查找/替换算法。如果您需要与引入高级查找/替换功能之前完全相同的行为，请使用此标志。请注意，旧算法不支持高级功能，例如替换为中断、应用格式等。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示使用旧的查找/替换算法。 |

### setMatchCase(boolean value) {#setMatchCase-boolean-}
```
public void setMatchCase(boolean value)
```


True 表示区分大小写比较，false 表示不区分大小写比较。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setReplacingCallback(IReplacingCallback value) {#setReplacingCallback-com.aspose.words.IReplacingCallback-}
```
public void setReplacingCallback(IReplacingCallback value)
```


在每次替换发生之前调用的用户定义方法。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IReplacingCallback](../../com.aspose.words/ireplacingcallback) | 相应的[IReplacingCallback](../../com.aspose.words/ireplacingcallback)价值。 |

### setSmartParagraphBreakReplacement(boolean value) {#setSmartParagraphBreakReplacement-boolean-}
```
public void setSmartParagraphBreakReplacement(boolean value)
```


获取或设置一个布尔值，指示是否允许在没有下一个同级段落时替换分段符。

默认值为 false 。

当没有下一个所有子节点都可以移动到的同级段落时，此选项允许通过在被替换的段落之后找到任何（不一定是同级）下一段来替换分段符。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUseLegacyOrder(boolean value) {#setUseLegacyOrder-boolean-}
```
public void setUseLegacyOrder(boolean value)
```


True 表示考虑文本框从上到下按顺序执行文本搜索。默认值为假。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUseSubstitutions(boolean value) {#setUseSubstitutions-boolean-}
```
public void setUseSubstitutions(boolean value)
```


设置一个布尔值，指示是否识别和使用替换模式中的替换。默认值为 false 。有关替换元素的详细信息，请参阅：https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示是否识别和使用替换模式中的替换。 |

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
