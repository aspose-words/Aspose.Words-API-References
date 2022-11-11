---
title: ListTemplate
second_title: Aspose.Words for Java API 参考
description: 指定 Microsoft Word 中可用的预定义列表格式之一。
type: docs
weight: 375
url: /zh/java/com.aspose.words/listtemplate/
---

**遗产:**
java.lang.Object
```
public class ListTemplate
```

指定 Microsoft Word 中可用的预定义列表格式之一。

列表模板值用作参数**M:Aspose.Words.Lists.ListCollection.Add(Aspose.Words.Lists.ListTemplate)**方法。

Aspose.Words 列表模板对应于 Microsoft Word 2003 中的“项目符号和编号”对话框中的 21 个列表模板。
## 字段

| 字段 | 描述 |
| --- | --- |
| [BULLET_ARROW_HEAD](#BULLET-ARROW-HEAD) | 第一关的子弹是箭头永定字。 |
| [BULLET_CIRCLE](#BULLET-CIRCLE) | 第一级的子弹是一个圆圈。 |
| [BULLET_DEFAULT](#BULLET-DEFAULT) | 具有 9 个级别的默认项目符号列表。 |
| [BULLET_DIAMONDS](#BULLET-DIAMONDS) | 第一关的子弹是一个4钻的Wingding角色。 |
| [BULLET_DISK](#BULLET-DISK) | 与 BulletDefault 相同。 |
| [BULLET_SQUARE](#BULLET-SQUARE) | 第一级的子弹是一个正方形。 |
| [BULLET_TICK](#BULLET-TICK) | 第一级的子弹是一个打勾的Wingding 字符。 |
| [NUMBER_ARABIC_DOT](#NUMBER-ARABIC-DOT) | 与 NumberDefault 相同。 |
| [NUMBER_ARABIC_PARENTHESIS](#NUMBER-ARABIC-PARENTHESIS) | 第一级的数字是“1)”。 |
| [NUMBER_DEFAULT](#NUMBER-DEFAULT) | 具有 9 个级别的默认编号列表。 |
| [NUMBER_LOWERCASE_LETTER_DOT](#NUMBER-LOWERCASE-LETTER-DOT) | 第一级的数字是“a.”。 |
| [NUMBER_LOWERCASE_LETTER_PARENTHESIS](#NUMBER-LOWERCASE-LETTER-PARENTHESIS) | 第一级的数字是“a)”。 |
| [NUMBER_LOWERCASE_ROMAN_DOT](#NUMBER-LOWERCASE-ROMAN-DOT) | 第一级的数字是“i.”。 |
| [NUMBER_UPPERCASE_LETTER_DOT](#NUMBER-UPPERCASE-LETTER-DOT) | 第一级的数字是“A.”。 |
| [NUMBER_UPPERCASE_ROMAN_DOT](#NUMBER-UPPERCASE-ROMAN-DOT) | 第一级的数字是“I.”。 |
| [OUTLINE_BULLETS](#OUTLINE-BULLETS) | 大纲列出了不同级别的各种项目符号。 |
| [OUTLINE_HEADINGS_ARTICLE_SECTION](#OUTLINE-HEADINGS-ARTICLE-SECTION) | 具有链接到标题样式的级别的大纲列表。 |
| [OUTLINE_HEADINGS_CHAPTER](#OUTLINE-HEADINGS-CHAPTER) | 具有链接到标题样式的级别的大纲列表。 |
| [OUTLINE_HEADINGS_LEGAL](#OUTLINE-HEADINGS-LEGAL) | 具有链接到标题样式的级别的大纲列表。 |
| [OUTLINE_HEADINGS_NUMBERS](#OUTLINE-HEADINGS-NUMBERS) | 具有链接到标题样式的级别的大纲列表。 |
| [OUTLINE_LEGAL](#OUTLINE-LEGAL) | 具有级别的大纲列表编号为“1., 1.1., 1.1.1, ...”。 |
| [OUTLINE_NUMBERS](#OUTLINE-NUMBERS) | 一个大纲列表，其级别编号为“1)、a)、i)、(1)、(a)、(i)、1.、a.、i.”。 |
| [length](#length) |  |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String listTemplateName)](#fromName-java.lang.String-) |  |
| [get班级()](#get班级--) |  |
| [getName(int listTemplate)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int listTemplate)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BULLET_ARROW_HEAD {#BULLET-ARROW-HEAD}
```
public static int BULLET_ARROW_HEAD
```


第一关的子弹是箭头永定字。其余级别与 BulletDefault 中的相同。

对应于 Microsoft Word 中的“项目符号和编号”对话框中的第 6 个项目符号列表模板。

### BULLET_CIRCLE {#BULLET-CIRCLE}
```
public static int BULLET_CIRCLE
```


第一级的子弹是一个圆圈。其余级别与 BulletDefault 中的相同。

对应于 Microsoft Word 中的项目符号和编号对话框中的第二个项目符号列表模板。

### BULLET_DEFAULT {#BULLET-DEFAULT}
```
public static int BULLET_DEFAULT
```


具有 9 个级别的默认项目符号列表。第一级子弹是圆盘，第二级子弹是圆形，第三级子弹是方形。然后对其余级别重复格式化。

每个级别相对于前一个级别向右缩进 0.25"。

对应于 Microsoft Word 中的项目符号和编号对话框中的第一个项目符号列表模板。

### BULLET_DIAMONDS {#BULLET-DIAMONDS}
```
public static int BULLET_DIAMONDS
```


第一关的子弹是一个4钻的Wingding角色。其余级别与 BulletDefault 中的相同。

对应于 Microsoft Word 中“项目符号和编号”对话框中的第 5 个项目符号列表模板。

### BULLET_DISK {#BULLET-DISK}
```
public static int BULLET_DISK
```


与 BulletDefault 相同。

对应于 Microsoft Word 中的项目符号和编号对话框中的第一个项目符号列表模板。

### BULLET_SQUARE {#BULLET-SQUARE}
```
public static int BULLET_SQUARE
```


第一级的子弹是一个正方形。其余级别与 BulletDefault 中的相同。

对应于 Microsoft Word 中“项目符号和编号”对话框中的第 3 个项目符号列表模板。

### BULLET_TICK {#BULLET-TICK}
```
public static int BULLET_TICK
```


第一级的子弹是一个打勾的Wingding 字符。其余级别与 BulletDefault 中的相同。

对应于 Microsoft Word 中“项目符号和编号”对话框中的第 7 个项目符号列表模板。

### NUMBER_ARABIC_DOT {#NUMBER-ARABIC-DOT}
```
public static int NUMBER_ARABIC_DOT
```


与 NumberDefault 相同。

对应于 Microsoft Word 中的项目符号和编号对话框中的第一个编号列表模板。

### NUMBER_ARABIC_PARENTHESIS {#NUMBER-ARABIC-PARENTHESIS}
```
public static int NUMBER_ARABIC_PARENTHESIS
```


第一级的数字是“1)”。其余级别与 NumberDefault 中的相同。

对应于 Microsoft Word 中的项目符号和编号对话框中的第二个编号列表模板。

### NUMBER_DEFAULT {#NUMBER-DEFAULT}
```
public static int NUMBER_DEFAULT
```


具有 9 个级别的默认编号列表。第一级为阿拉伯编号（1., 2., 3., ...），第二级为小写字母编号（a., b., c., ...），小写罗马编号（i., ii., iii., ...) 用于第三级。然后对其余级别重复格式化。

每个级别相对于前一个级别向右缩进 0.25"。

对应于 Microsoft Word 中的项目符号和编号对话框中的第一个编号列表模板。

### NUMBER_LOWERCASE_LETTER_DOT {#NUMBER-LOWERCASE-LETTER-DOT}
```
public static int NUMBER_LOWERCASE_LETTER_DOT
```


第一级的数字是“a.”。其余级别与 NumberDefault 中的相同。

对应于 Microsoft Word 中的“项目符号和编号”对话框中的第 6 个编号列表模板。

### NUMBER_LOWERCASE_LETTER_PARENTHESIS {#NUMBER-LOWERCASE-LETTER-PARENTHESIS}
```
public static int NUMBER_LOWERCASE_LETTER_PARENTHESIS
```


第一级的数字是“a)”。其余级别与 NumberDefault 中的相同。

对应于 Microsoft Word 中“项目符号和编号”对话框中的第 5 个编号列表模板。

### NUMBER_LOWERCASE_ROMAN_DOT {#NUMBER-LOWERCASE-ROMAN-DOT}
```
public static int NUMBER_LOWERCASE_ROMAN_DOT
```


第一级的数字是“i.”。其余级别与 NumberDefault 中的相同。

对应于 Microsoft Word 中的“项目符号和编号”对话框中的第 7 个编号列表模板。

### NUMBER_UPPERCASE_LETTER_DOT {#NUMBER-UPPERCASE-LETTER-DOT}
```
public static int NUMBER_UPPERCASE_LETTER_DOT
```


第一级的数字是“A.”。其余级别与 NumberDefault 中的相同。

对应于 Microsoft Word 中“项目符号和编号”对话框中的第 4 个编号列表模板。

### NUMBER_UPPERCASE_ROMAN_DOT {#NUMBER-UPPERCASE-ROMAN-DOT}
```
public static int NUMBER_UPPERCASE_ROMAN_DOT
```


第一级的数字是“I.”。其余级别与 NumberDefault 中的相同。

对应于 Microsoft Word 的“项目符号和编号”对话框中的第 3 个编号列表模板。

### OUTLINE_BULLETS {#OUTLINE-BULLETS}
```
public static int OUTLINE_BULLETS
```


大纲列出了不同级别的各种项目符号。

对应于 Microsoft Word 中的“项目符号和编号”对话框中的第 3 个大纲列表模板。

### OUTLINE_HEADINGS_ARTICLE_SECTION {#OUTLINE-HEADINGS-ARTICLE-SECTION}
```
public static int OUTLINE_HEADINGS_ARTICLE_SECTION
```


具有链接到标题样式的级别的大纲列表。

对应于 Microsoft Word 中的“项目符号和编号”对话框中的第 4 个大纲列表模板。

### OUTLINE_HEADINGS_CHAPTER {#OUTLINE-HEADINGS-CHAPTER}
```
public static int OUTLINE_HEADINGS_CHAPTER
```


具有链接到标题样式的级别的大纲列表。

对应于 Microsoft Word 中的项目符号和编号对话框中的第 7 个大纲列表模板。

### OUTLINE_HEADINGS_LEGAL {#OUTLINE-HEADINGS-LEGAL}
```
public static int OUTLINE_HEADINGS_LEGAL
```


具有链接到标题样式的级别的大纲列表。

对应于 Microsoft Word 中的项目符号和编号对话框中的第 5 个大纲列表模板。

### OUTLINE_HEADINGS_NUMBERS {#OUTLINE-HEADINGS-NUMBERS}
```
public static int OUTLINE_HEADINGS_NUMBERS
```


具有链接到标题样式的级别的大纲列表。

对应于 Microsoft Word 中的项目符号和编号对话框中的第 6 个大纲列表模板。

### OUTLINE_LEGAL {#OUTLINE-LEGAL}
```
public static int OUTLINE_LEGAL
```


具有级别的大纲列表编号为“1., 1.1., 1.1.1, ...”。

对应于 Microsoft Word 中的项目符号和编号对话框中的第二个大纲列表模板。

### OUTLINE_NUMBERS {#OUTLINE-NUMBERS}
```
public static int OUTLINE_NUMBERS
```


一个大纲列表，其级别编号为“1)、a)、i)、(1)、(a)、(i)、1.、a.、i.”。

对应于 Microsoft Word 中的项目符号和编号对话框中的第一个大纲列表模板。

### length {#length}
```
public static int length
```


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
### fromName(String listTemplateName) {#fromName-java.lang.String-}
```
public static int fromName(String listTemplateName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| listTemplateName | java.lang.String |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int listTemplate) {#getName-int-}
```
public static String getName(int listTemplate)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| listTemplate | int |  |

**退货:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**退货:**
整数[]
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




### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### toString(int listTemplate) {#toString-int-}
```
public static String toString(int listTemplate)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| listTemplate | int |  |

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
