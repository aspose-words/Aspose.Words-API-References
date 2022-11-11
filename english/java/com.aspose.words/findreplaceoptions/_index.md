---
title: FindReplaceOptions
second_title: Aspose.Words for Java API 参考
description: 指定查找/替换操作的选项。
type: docs
weight: 270
url: /zh/java/com.aspose.words/findreplaceoptions/
---

**遗产:**
java.lang.Object
```
public class FindReplaceOptions
```

指定查找/替换操作的选项。

要了解更多信息，请访问**Find and Replace**文档文章。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [FindReplaceOptions()](#FindReplaceOptions--) | 初始化此类的新实例。 |
| [FindReplaceOptions(int direction)](#FindReplaceOptions-int-) | 初始化此类的新实例。 |
| [FindReplaceOptions(IReplacingCallback replacingCallback)](#FindReplaceOptions-com.aspose.words.IReplacingCallback-) | 初始化此类的新实例。 |
| [FindReplaceOptions(int direction, IReplacingCallback replacingCallback)](#FindReplaceOptions-int-com.aspose.words.IReplacingCallback-) | 初始化此类的新实例。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getApplyFont()](#getApplyFont--) | 应用于新内容的文本格式。 |
| [getApplyParagraphFormat()](#getApplyParagraphFormat--) | 应用于新内容的段落格式。 |
| [get班级()](#get班级--) |  |
| [getDirection()](#getDirection--) | 选择替换方向。 |
| [getFindWholeWordsOnly()](#getFindWholeWordsOnly--) | True 表示 oldValue 必须是一个独立的单词。 |
| [getIgnoreDeleted()](#getIgnoreDeleted--) | 获取一个布尔值，指示是否忽略删除修订中的文本。 |
| [getIgnore字段Codes()](#getIgnore字段Codes--) | 获取一个布尔值，指示是否忽略域代码中的文本。 |
| [getIgnore字段()](#getIgnore字段--) | 获取一个布尔值，指示是否忽略字段内的文本。 |
| [getIgnoreFootnotes()](#getIgnoreFootnotes--) | 获取一个布尔值，指示要么忽略脚注。 |
| [getIgnoreInserted()](#getIgnoreInserted--) | 获取一个布尔值，指示是否忽略插入修订中的文本。 |
| [getIgnoreStructuredDocumentTags()](#getIgnoreStructuredDocumentTags--) | 获取一个布尔值，指示是否忽略[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag). |
| [getLegacyMode()](#getLegacyMode--) | 获取一个布尔值，指示使用旧的查找/替换算法。 |
| [getMatchCase()](#getMatchCase--) | True 表示区分大小写比较，false 表示不区分大小写比较。 |
| [getReplacingCallback()](#getReplacingCallback--) | 在每次替换发生之前调用的用户定义方法。 |
| [getSmartParagraphBreakReplacement()](#getSmartParagraphBreakReplacement--) | 获取或设置一个布尔值，指示在没有下一个同级段落时是否允许替换段落分隔符。 |
| [getUseLegacyOrder()](#getUseLegacyOrder--) | True 表示考虑到文本框，从上到下顺序执行文本搜索。 |
| [getUseSubstitutions()](#getUseSubstitutions--) | 获取一个布尔值，该值指示是否在替换模式中识别和使用替换。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setDirection(int value)](#setDirection-int-) | 选择替换方向。 |
| [setFindWholeWordsOnly(boolean value)](#setFindWholeWordsOnly-boolean-) | True 表示 oldValue 必须是一个独立的单词。 |
| [setIgnoreDeleted(boolean value)](#setIgnoreDeleted-boolean-) | 设置一个布尔值，指示忽略删除修订中的文本。 |
| [setIgnore字段Codes(boolean value)](#setIgnore字段Codes-boolean-) | 设置一个布尔值，指示忽略域代码内的文本。 |
| [setIgnore字段(boolean value)](#setIgnore字段-boolean-) | 设置一个布尔值，指示忽略字段内的文本。 |
| [setIgnoreFootnotes(boolean value)](#setIgnoreFootnotes-boolean-) | 设置一个布尔值，指示忽略脚注。 |
| [setIgnoreInserted(boolean value)](#setIgnoreInserted-boolean-) | 设置一个布尔值，指示忽略插入修订中的文本。 |
| [setIgnoreStructuredDocumentTags(boolean value)](#setIgnoreStructuredDocumentTags-boolean-) | 设置一个布尔值，指示要么忽略[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag). |
| [setLegacyMode(boolean value)](#setLegacyMode-boolean-) | 设置一个布尔值，指示使用旧的查找/替换算法。 |
| [setMatchCase(boolean value)](#setMatchCase-boolean-) | True 表示区分大小写比较，false 表示不区分大小写比较。 |
| [setReplacingCallback(IReplacingCallback value)](#setReplacingCallback-com.aspose.words.IReplacingCallback-) | 在每次替换发生之前调用的用户定义方法。 |
| [setSmartParagraphBreakReplacement(boolean value)](#setSmartParagraphBreakReplacement-boolean-) | 获取或设置一个布尔值，指示在没有下一个同级段落时是否允许替换段落分隔符。 |
| [setUseLegacyOrder(boolean value)](#setUseLegacyOrder-boolean-) | True 表示考虑到文本框，从上到下顺序执行文本搜索。 |
| [setUseSubstitutions(boolean value)](#setUseSubstitutions-boolean-) | 设置一个布尔值，指示是否在替换模式中识别和使用替换。 |
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

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| direction | int |  |

### FindReplaceOptions(IReplacingCallback replacingCallback) {#FindReplaceOptions-com.aspose.words.IReplacingCallback-}
```
public FindReplaceOptions(IReplacingCallback replacingCallback)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback) |  |

### FindReplaceOptions(int direction, IReplacingCallback replacingCallback) {#FindReplaceOptions-int-com.aspose.words.IReplacingCallback-}
```
public FindReplaceOptions(int direction, IReplacingCallback replacingCallback)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| direction | int |  |
| replacingCallback | [IReplacingCallback](../../com.aspose.words/ireplacingcallback) |  |

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
### getApplyFont() {#getApplyFont--}
```
public Font getApplyFont()
```


应用于新内容的文本格式。

**退货:**
[Font](../../com.aspose.words/font) - 相应的[Font](../../com.aspose.words/font)价值。
### getApplyParagraphFormat() {#getApplyParagraphFormat--}
```
public ParagraphFormat getApplyParagraphFormat()
```


应用于新内容的段落格式。

**退货:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - 相应的[ParagraphFormat](../../com.aspose.words/paragraphformat)价值。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getDirection() {#getDirection--}
```
public int getDirection()
```


选择替换方向。默认值为[FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection\#FORWARD).

**退货:**
int - 对应的 int 值。返回值是以下之一[FindReplaceDirection](../../com.aspose.words/findreplacedirection)常数。
### getFindWholeWordsOnly() {#getFindWholeWordsOnly--}
```
public boolean getFindWholeWordsOnly()
```


True 表示 oldValue 必须是一个独立的单词。

**退货:**
boolean - 对应的布尔值。
### getIgnoreDeleted() {#getIgnoreDeleted--}
```
public boolean getIgnoreDeleted()
```


获取一个布尔值，指示是否忽略删除修订中的文本。默认值为 false 。

**退货:**
boolean - 一个布尔值，指示忽略删除修订中的文本。
### getIgnore字段Codes() {#getIgnore字段Codes--}
```
public boolean getIgnore字段Codes()
```


获取一个布尔值，指示是否忽略域代码中的文本。默认值为 false 。

此选项仅影响域代码（它不会忽略[Node类型.FIELD\_SEPARATOR](../../com.aspose.words/nodetype\#FIELD-SEPARATOR)和[Node类型.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END)）。

要忽略整个字段，请使用相应的选项[getIgnore字段()](../../com.aspose.words/findreplaceoptions\#getIgnore字段--) / [setIgnore字段(boolean)](../../com.aspose.words/findreplaceoptions\#setIgnore字段-boolean-).

**退货:**
boolean - 一个布尔值，指示忽略域代码内的文本。
### getIgnore字段() {#getIgnore字段--}
```
public boolean getIgnore字段()
```


获取一个布尔值，指示是否忽略字段内的文本。默认值为 false 。

此选项影响整个字段（之间的所有节点[Node类型.FIELD\_START](../../com.aspose.words/nodetype\#FIELD-START)和[Node类型.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END)）。

要仅忽略域代码，请使用相应的选项[getIgnore字段Codes()](../../com.aspose.words/findreplaceoptions\#getIgnore字段Codes--) / [setIgnore字段Codes(boolean)](../../com.aspose.words/findreplaceoptions\#setIgnore字段Codes-boolean-).

**退货:**
boolean - 一个布尔值，指示忽略字段内的文本。
### getIgnoreFootnotes() {#getIgnoreFootnotes--}
```
public boolean getIgnoreFootnotes()
```


获取一个布尔值，指示要么忽略脚注。默认值为 false 。

**退货:**
boolean - 一个布尔值，指示忽略脚注。
### getIgnoreInserted() {#getIgnoreInserted--}
```
public boolean getIgnoreInserted()
```


获取一个布尔值，指示是否忽略插入修订中的文本。默认值为 false 。

**退货:**
boolean - 一个布尔值，指示忽略插入修订中的文本。
### getIgnoreStructuredDocumentTags() {#getIgnoreStructuredDocumentTags--}
```
public boolean getIgnoreStructuredDocumentTags()
```


获取一个布尔值，指示是否忽略[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag).默认值为 false 。

当此选项设置为 true 时，[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)将被视为简单文本。

否则，[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)将作为独立故事处理，替换模式将分别搜索每个[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)，所以如果模式穿过[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)，则不会对此类模式执行替换。

**退货:**
 boolean - 一个布尔值，表示忽略[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag).
### getLegacyMode() {#getLegacyMode--}
```
public boolean getLegacyMode()
```


获取一个布尔值，指示使用旧的查找/替换算法。如果您需要与引入高级查找/替换功能之前完全相同的行为，请使用此标志。请注意，旧算法不支持高级功能，例如用换行符替换、应用格式等。

**退货:**
boolean - 一个布尔值，指示使用旧的查找/替换算法。
### getMatchCase() {#getMatchCase--}
```
public boolean getMatchCase()
```


True 表示区分大小写比较，false 表示不区分大小写比较。

**退货:**
boolean - 对应的布尔值。
### getReplacingCallback() {#getReplacingCallback--}
```
public IReplacingCallback getReplacingCallback()
```


在每次替换发生之前调用的用户定义方法。

**退货:**
[IReplacingCallback](../../com.aspose.words/ireplacingcallback) - 相应的[IReplacingCallback](../../com.aspose.words/ireplacingcallback)价值。
### getSmartParagraphBreakReplacement() {#getSmartParagraphBreakReplacement--}
```
public boolean getSmartParagraphBreakReplacement()
```


获取或设置一个布尔值，指示在没有下一个同级段落时是否允许替换段落分隔符。

默认值为 false 。

此选项允许在没有可以将所有子节点移动到的下一个兄弟段落时替换段落分隔符，方法是在被替换的段落之后查找任何（不一定是兄弟）下一个段落。

**退货:**
boolean - 对应的布尔值。
### getUseLegacyOrder() {#getUseLegacyOrder--}
```
public boolean getUseLegacyOrder()
```


True 表示考虑到文本框，从上到下顺序执行文本搜索。默认值为假。

**退货:**
boolean - 对应的布尔值。
### getUseSubstitutions() {#getUseSubstitutions--}
```
public boolean getUseSubstitutions()
```


获取一个布尔值，该值指示是否在替换模式中识别和使用替换。默认值为 false 。有关替换元素的详细信息，请参阅：https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions。

**退货:**
boolean - 一个布尔值，指示是否在替换模式中识别和使用替换。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




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




### setDirection(int value) {#setDirection-int-}
```
public void setDirection(int value)
```


选择替换方向。默认值为[FindReplaceDirection.FORWARD](../../com.aspose.words/findreplacedirection\#FORWARD).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[FindReplaceDirection](../../com.aspose.words/findreplacedirection)常数。 |

### setFindWholeWordsOnly(boolean value) {#setFindWholeWordsOnly-boolean-}
```
public void setFindWholeWordsOnly(boolean value)
```


True 表示 oldValue 必须是一个独立的单词。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setIgnoreDeleted(boolean value) {#setIgnoreDeleted-boolean-}
```
public void setIgnoreDeleted(boolean value)
```


设置一个布尔值，指示忽略删除修订中的文本。默认值为 false 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示忽略删除修订中的文本。 |

### setIgnore字段Codes(boolean value) {#setIgnore字段Codes-boolean-}
```
public void setIgnore字段Codes(boolean value)
```


设置一个布尔值，指示忽略域代码内的文本。默认值为 false 。

此选项仅影响域代码（它不会忽略[Node类型.FIELD\_SEPARATOR](../../com.aspose.words/nodetype\#FIELD-SEPARATOR)和[Node类型.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END)）。

要忽略整个字段，请使用相应的选项[getIgnore字段()](../../com.aspose.words/findreplaceoptions\#getIgnore字段--) / [setIgnore字段(boolean)](../../com.aspose.words/findreplaceoptions\#setIgnore字段-boolean-).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示忽略域代码内的文本。 |

### setIgnore字段(boolean value) {#setIgnore字段-boolean-}
```
public void setIgnore字段(boolean value)
```


设置一个布尔值，指示忽略字段内的文本。默认值为 false 。

此选项影响整个字段（之间的所有节点[Node类型.FIELD\_START](../../com.aspose.words/nodetype\#FIELD-START)和[Node类型.FIELD\_END](../../com.aspose.words/nodetype\#FIELD-END)）。

要仅忽略域代码，请使用相应的选项[getIgnore字段Codes()](../../com.aspose.words/findreplaceoptions\#getIgnore字段Codes--) / [setIgnore字段Codes(boolean)](../../com.aspose.words/findreplaceoptions\#setIgnore字段Codes-boolean-).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示忽略字段内的文本。 |

### setIgnoreFootnotes(boolean value) {#setIgnoreFootnotes-boolean-}
```
public void setIgnoreFootnotes(boolean value)
```


设置一个布尔值，指示忽略脚注。默认值为 false 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示忽略脚注。 |

### setIgnoreInserted(boolean value) {#setIgnoreInserted-boolean-}
```
public void setIgnoreInserted(boolean value)
```


设置一个布尔值，指示忽略插入修订中的文本。默认值为 false 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示忽略插入修订中的文本。 |

### setIgnoreStructuredDocumentTags(boolean value) {#setIgnoreStructuredDocumentTags-boolean-}
```
public void setIgnoreStructuredDocumentTags(boolean value)
```


设置一个布尔值，指示要么忽略[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag).默认值为 false 。

当此选项设置为 true 时，[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)将被视为简单文本。

否则，[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)将作为独立故事处理，替换模式将分别搜索每个[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)，所以如果模式穿过[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)，则不会对此类模式执行替换。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示要么忽略[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag). |

### setLegacyMode(boolean value) {#setLegacyMode-boolean-}
```
public void setLegacyMode(boolean value)
```


设置一个布尔值，指示使用旧的查找/替换算法。如果您需要与引入高级查找/替换功能之前完全相同的行为，请使用此标志。请注意，旧算法不支持高级功能，例如用换行符替换、应用格式等。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示使用旧的查找/替换算法。 |

### setMatchCase(boolean value) {#setMatchCase-boolean-}
```
public void setMatchCase(boolean value)
```


True 表示区分大小写比较，false 表示不区分大小写比较。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setReplacingCallback(IReplacingCallback value) {#setReplacingCallback-com.aspose.words.IReplacingCallback-}
```
public void setReplacingCallback(IReplacingCallback value)
```


在每次替换发生之前调用的用户定义方法。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IReplacingCallback](../../com.aspose.words/ireplacingcallback) | 相应的[IReplacingCallback](../../com.aspose.words/ireplacingcallback)价值。 |

### setSmartParagraphBreakReplacement(boolean value) {#setSmartParagraphBreakReplacement-boolean-}
```
public void setSmartParagraphBreakReplacement(boolean value)
```


获取或设置一个布尔值，指示在没有下一个同级段落时是否允许替换段落分隔符。

默认值为 false 。

此选项允许在没有可以将所有子节点移动到的下一个兄弟段落时替换段落分隔符，方法是在被替换的段落之后查找任何（不一定是兄弟）下一个段落。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUseLegacyOrder(boolean value) {#setUseLegacyOrder-boolean-}
```
public void setUseLegacyOrder(boolean value)
```


True 表示考虑到文本框，从上到下顺序执行文本搜索。默认值为假。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUseSubstitutions(boolean value) {#setUseSubstitutions-boolean-}
```
public void setUseSubstitutions(boolean value)
```


设置一个布尔值，指示是否在替换模式中识别和使用替换。默认值为 false 。有关替换元素的详细信息，请参阅：https://docs.microsoft.com/en-us/dotnet/standard/base-types/substitutions-in-regular-expressions。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，指示是否在替换模式中识别和使用替换。 |

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
