---
title: Image字段MergingArgs
second_title: Aspose.Words for Java API 参考
description: 为事件提供数据。
type: docs
weight: 338
url: /zh/java/com.aspose.words/imagefieldmergingargs/
---

**遗产:**
java.lang.Object, [com.aspose.words.字段MergingArgsBase](../../com.aspose.words/fieldmergingargsbase)
```
public class Image字段MergingArgs extends 字段MergingArgsBase
```

提供数据为[I字段MergingCallback.image字段Merging(com.aspose.words.Image字段MergingArgs)](../../com.aspose.words/ifieldmergingcallback\#image字段Merging-com.aspose.words.Image字段MergingArgs-)事件。

要了解更多信息，请访问**Mail Merge and Reporting**文档文章。

当在文档中遇到图像邮件合并字段时，在邮件合并期间发生此事件。您可以响应此事件以将文件名、流或 java.awt.image.BufferedImage 对象返回给邮件合并引擎，以便将其插入到文档中。

共有三个属性可用[getImageFileName()](../../com.aspose.words/imagefieldmergingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs\#setImageFileName-java.lang.String-), **P:Aspose.Words.MailMerging.Image字段MergingArgs.ImageStream**和[getImage()](../../com.aspose.words/imagefieldmergingargs\#getImage--) / [setImage(java.awt.image.BufferedImage)](../../com.aspose.words/imagefieldmergingargs\#setImage-java.awt.image.BufferedImage-)指定必须从哪里获取图像。仅设置这些属性之一。

要将图像邮件合并字段插入 Word 中的文档，请选择插入/字段命令，然后选择 Merge字段 并键入 Image:My字段Name。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getDocument()](#getDocument--) | 返回[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--)执行邮件合并的对象。 |
| [getDocument字段Name()](#getDocument字段Name--) | 获取文档中指定的合并字段的名称。 |
| [get字段()](#get字段--) | 获取表示当前合并字段的对象。 |
| [get字段Name()](#get字段Name--) | 获取数据源中合并字段的名称。 |
| [get字段Value()](#get字段Value--) | 从数据源获取字段的值。 |
| [getImage()](#getImage--) | 指定邮件合并引擎必须插入到文档中的图像。 |
| [getImageFileName()](#getImageFileName--) | 设置邮件合并引擎必须插入到文档中的图像的文件名。 |
| [getImageHeight()](#getImageHeight--) | 指定要插入到文档中的图像的图像高度。 |
| [getImageStream()](#getImageStream--) |  |
| [getImageWidth()](#getImageWidth--) | 指定要插入到文档中的图像的图像宽度。 |
| [getRecordIndex()](#getRecordIndex--) | 获取正在合并的记录的从零开始的索引。 |
| [getShape()](#getShape--) | 指定邮件合并引擎必须插入到文档中的形状。 |
| [getTableName()](#getTableName--) | 获取当前合并操作的数据表的名称，如果名称不可用，则为空字符串。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [set字段Value(Object value)](#set字段Value-java.lang.Object-) | 设置数据源中字段的值。 |
| [setImage(BufferedImage value)](#setImage-java.awt.image.BufferedImage-) | 指定邮件合并引擎必须插入到文档中的图像。 |
| [setImageFileName(String value)](#setImageFileName-java.lang.String-) | 设置邮件合并引擎必须插入到文档中的图像的文件名。 |
| [setImageHeight(Merge字段ImageDimension value)](#setImageHeight-com.aspose.words.Merge字段ImageDimension-) | 指定要插入到文档中的图像的图像高度。 |
| [setImageStream(InputStream value)](#setImageStream-java.io.InputStream-) |  |
| [setImageWidth(Merge字段ImageDimension value)](#setImageWidth-com.aspose.words.Merge字段ImageDimension-) | 指定要插入到文档中的图像的图像宽度。 |
| [setShape(Shape value)](#setShape-com.aspose.words.Shape-) | 指定邮件合并引擎必须插入到文档中的形状。 |
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
### getDocument() {#getDocument--}
```
public Document getDocument()
```


返回[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--)执行邮件合并的对象。

**退货:**
[Document](../../com.aspose.words/document) - 这[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--)执行邮件合并的对象。
### getDocument字段Name() {#getDocument字段Name--}
```
public String getDocument字段Name()
```


获取文档中指定的合并字段的名称。

如果您有从文档字段名称到不同数据源字段名称的映射，则这是文档中指定的原始字段名称。

如果您在文档中指定了字段名称前缀，例如“Image:My字段Name”，则**Document字段Name**返回不带前缀的字段名称，即“My字段Name”。

**退货:**
java.lang.String - 文档中指定的合并字段的名称。
### get字段() {#get字段--}
```
public 字段Merge字段 get字段()
```


获取表示当前合并字段的对象。

**退货:**
[字段Merge字段](../../com.aspose.words/fieldmergefield) - 表示当前合并字段的对象。
### get字段Name() {#get字段Name--}
```
public String get字段Name()
```


获取数据源中合并字段的名称。

如果您有从文档字段名称到不同数据源字段名称的映射，那么这就是映射的字段名称。

如果您在文档中指定了字段名称前缀，例如“Image:My字段Name”，则**字段Name**返回不带前缀的字段名称，即“My字段Name”。

**退货:**
java.lang.String - 数据源中合并字段的名称。
### get字段Value() {#get字段Value--}
```
public Object get字段Value()
```


从数据源获取字段的值。此属性包含邮件合并引擎刚刚从您的数据源中为此字段选择的值。您还可以通过设置属性来替换该值。

**退货:**
java.lang.Object - 数据源中的字段值。
### getImage() {#getImage--}
```
public BufferedImage getImage()
```


指定邮件合并引擎必须插入到文档中的图像。

**退货:**
java.awt.image.BufferedImage - 对应的 java.awt.image.BufferedImage 值。
### getImageFileName() {#getImageFileName--}
```
public String getImageFileName()
```


设置邮件合并引擎必须插入到文档中的图像的文件名。

**退货:**
java.lang.String - 邮件合并引擎必须插入到文档中的图像文件名。
### getImageHeight() {#getImageHeight--}
```
public Merge字段ImageDimension getImageHeight()
```


指定要插入到文档中的图像的图像高度。

此属性的值最初来自模板文档中包含的相应 MERGEFIELD 的代码。要覆盖初始值，您应该分配一个实例[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension)类到此属性或设置实例的属性[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension)类，由该属性返回。

要指示应该应用图像高度的原始值，您应该分配**null**该属性的值或设置[Merge字段ImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [Merge字段ImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-)实例的属性[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension)由该属性返回的类为负值。

**退货:**
[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension) - 相应的[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension)价值。
### getImageStream() {#getImageStream--}
```
public InputStream getImageStream()
```




**退货:**
java.io.InputStream
### getImageWidth() {#getImageWidth--}
```
public Merge字段ImageDimension getImageWidth()
```


指定要插入到文档中的图像的图像宽度。

此属性的值最初来自模板文档中包含的相应 MERGEFIELD 的代码。要覆盖初始值，您应该分配一个实例[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension)类到此属性或设置实例的属性[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension)类，由该属性返回。

要指示应应用图像宽度的原始值，您应该分配**null**该属性的值或设置[Merge字段ImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [Merge字段ImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-)实例的属性[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension)由该属性返回的类为负值。

**退货:**
[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension) - 相应的[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension)价值。
### getRecordIndex() {#getRecordIndex--}
```
public int getRecordIndex()
```


获取正在合并的记录的从零开始的索引。

**退货:**
int - 正在合并的记录的从零开始的索引。
### getShape() {#getShape--}
```
public Shape getShape()
```


指定邮件合并引擎必须插入到文档中的形状。

指定此属性时，邮件合并引擎会忽略所有其他属性，例如[getImageFileName()](../../com.aspose.words/imagefieldmergingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs\#setImageFileName-java.lang.String-)或者**P:Aspose.Words.MailMerging.Image字段MergingArgs.ImageStream**并简单地将形状插入到文档中。

使用此属性可以完全控制合并图像合并字段的过程。例如，您可以指定[ShapeBase.getWrap类型()](../../com.aspose.words/shapebase\#getWrap类型--) / [ShapeBase.setWrap类型(int)](../../com.aspose.words/shapebase\#setWrap类型-int-)或任何其他形状属性来微调结果节点。但是，请注意，您有责任提供形状的内容。

**退货:**
[Shape](../../com.aspose.words/shape) - 相应的[Shape](../../com.aspose.words/shape)价值。
### getTableName() {#getTableName--}
```
public String getTableName()
```


获取当前合并操作的数据表的名称，如果名称不可用，则为空字符串。

**退货:**
java.lang.String - 当前合并操作的数据表的名称，如果名称不可用，则为空字符串。
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




### set字段Value(Object value) {#set字段Value-java.lang.Object-}
```
public void set字段Value(Object value)
```


设置数据源中字段的值。此属性包含邮件合并引擎刚刚从您的数据源中为此字段选择的值。您还可以通过设置属性来替换该值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.Object | 数据源中的字段值。 |

### setImage(BufferedImage value) {#setImage-java.awt.image.BufferedImage-}
```
public void setImage(BufferedImage value)
```


指定邮件合并引擎必须插入到文档中的图像。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.image.BufferedImage | 对应的 java.awt.image.BufferedImage 值。 |

### setImageFileName(String value) {#setImageFileName-java.lang.String-}
```
public void setImageFileName(String value)
```


设置邮件合并引擎必须插入到文档中的图像的文件名。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 邮件合并引擎必须插入到文档中的图像的文件名。 |

### setImageHeight(Merge字段ImageDimension value) {#setImageHeight-com.aspose.words.Merge字段ImageDimension-}
```
public void setImageHeight(Merge字段ImageDimension value)
```


指定要插入到文档中的图像的图像高度。

此属性的值最初来自模板文档中包含的相应 MERGEFIELD 的代码。要覆盖初始值，您应该分配一个实例[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension)类到此属性或设置实例的属性[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension)类，由该属性返回。

要指示应该应用图像高度的原始值，您应该分配**null**该属性的值或设置[Merge字段ImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [Merge字段ImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-)实例的属性[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension)由该属性返回的类为负值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension) | 相应的[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension)价值。 |

### setImageStream(InputStream value) {#setImageStream-java.io.InputStream-}
```
public void setImageStream(InputStream value)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.io.InputStream |  |

### setImageWidth(Merge字段ImageDimension value) {#setImageWidth-com.aspose.words.Merge字段ImageDimension-}
```
public void setImageWidth(Merge字段ImageDimension value)
```


指定要插入到文档中的图像的图像宽度。

此属性的值最初来自模板文档中包含的相应 MERGEFIELD 的代码。要覆盖初始值，您应该分配一个实例[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension)类到此属性或设置实例的属性[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension)类，由该属性返回。

要指示应应用图像宽度的原始值，您应该分配**null**该属性的值或设置[Merge字段ImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [Merge字段ImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-)实例的属性[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension)由该属性返回的类为负值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension) | 相应的[Merge字段ImageDimension](../../com.aspose.words/mergefieldimagedimension)价值。 |

### setShape(Shape value) {#setShape-com.aspose.words.Shape-}
```
public void setShape(Shape value)
```


指定邮件合并引擎必须插入到文档中的形状。

指定此属性时，邮件合并引擎会忽略所有其他属性，例如[getImageFileName()](../../com.aspose.words/imagefieldmergingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs\#setImageFileName-java.lang.String-)或者**P:Aspose.Words.MailMerging.Image字段MergingArgs.ImageStream**并简单地将形状插入到文档中。

使用此属性可以完全控制合并图像合并字段的过程。例如，您可以指定[ShapeBase.getWrap类型()](../../com.aspose.words/shapebase\#getWrap类型--) / [ShapeBase.setWrap类型(int)](../../com.aspose.words/shapebase\#setWrap类型-int-)或任何其他形状属性来微调结果节点。但是，请注意，您有责任提供形状的内容。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape) | 相应的[Shape](../../com.aspose.words/shape)价值。 |

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
