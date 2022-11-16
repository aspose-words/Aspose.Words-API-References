---
title: ImageFieldMergingArgs
second_title: Aspose.Words for Java API 参考
description: 为事件提供数据。
type: docs
weight: 338
url: /zh/java/com.aspose.words/imagefieldmergingargs/
---

**遗产：**
java.lang.Object, [com.aspose.words.FieldMergingArgsBase](../../com.aspose.words/fieldmergingargsbase)
```
public class ImageFieldMergingArgs extends FieldMergingArgsBase
```

提供数据[IFieldMergingCallback.imageFieldMerging(com.aspose.words.ImageFieldMergingArgs)](../../com.aspose.words/ifieldmergingcallback\#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs-)事件。

要了解更多信息，请访问**Mail Merge and Reporting**文档文章。

当在文档中遇到图像邮件合并域时，邮件合并期间会发生此事件。您可以响应此事件以将文件名、流或 java.awt.image.BufferedImage 对象返回到邮件合并引擎，以便将其插入到文档中。

提供三个属性[getImageFileName()](../../com.aspose.words/imagefieldmergingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs\#setImageFileName-java.lang.String-), **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream**和[getImage()](../../com.aspose.words/imagefieldmergingargs\#getImage--) / [setImage(java.awt.image.BufferedImage)](../../com.aspose.words/imagefieldmergingargs\#setImage-java.awt.image.BufferedImage-)指定必须从何处获取图像。仅设置这些属性之一。

要将图像邮件合并域插入到 Word 文档中，请选择插入/域命令，然后选择 MergeField 并键入 Image:MyFieldName。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDocument()](#getDocument--) | 返回[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--)执行邮件合并的对象。 |
| [getDocumentFieldName()](#getDocumentFieldName--) | 获取文档中指定的合并字段的名称。 |
| [getField()](#getField--) | 获取表示当前合并字段的对象。 |
| [getFieldName()](#getFieldName--) | 获取数据源中合并字段的名称。 |
| [getFieldValue()](#getFieldValue--) | 从数据源中获取字段的值。 |
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
| [setFieldValue(Object value)](#setFieldValue-java.lang.Object-) | 设置来自数据源的字段值。 |
| [setImage(BufferedImage value)](#setImage-java.awt.image.BufferedImage-) | 指定邮件合并引擎必须插入到文档中的图像。 |
| [setImageFileName(String value)](#setImageFileName-java.lang.String-) | 设置邮件合并引擎必须插入到文档中的图像的文件名。 |
| [setImageHeight(MergeFieldImageDimension value)](#setImageHeight-com.aspose.words.MergeFieldImageDimension-) | 指定要插入到文档中的图像的图像高度。 |
| [setImageStream(InputStream value)](#setImageStream-java.io.InputStream-) |  |
| [setImageWidth(MergeFieldImageDimension value)](#setImageWidth-com.aspose.words.MergeFieldImageDimension-) | 指定要插入到文档中的图像的图像宽度。 |
| [setShape(Shape value)](#setShape-com.aspose.words.Shape-) | 指定邮件合并引擎必须插入到文档中的形状。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getDocument() {#getDocument--}
```
public Document getDocument()
```


返回[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--)执行邮件合并的对象。

**退货：**
[Document](../../com.aspose.words/document) - 这[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--)执行邮件合并的对象。
### getDocumentFieldName() {#getDocumentFieldName--}
```
public String getDocumentFieldName()
```


获取文档中指定的合并字段的名称。

如果您有从文档字段名称到不同数据源字段名称的映射，那么这是文档中指定的原始字段名称。

如果您在文档中指定了字段名称前缀，例如“Image:MyFieldName”，则**DocumentFieldName**返回不带前缀的字段名称，即“MyFieldName”。

**退货：**
java.lang.String - 文档中指定的合并字段的名称。
### getField() {#getField--}
```
public FieldMergeField getField()
```


获取表示当前合并字段的对象。

**退货：**
[FieldMergeField](../../com.aspose.words/fieldmergefield) - 表示当前合并字段的对象。
### getFieldName() {#getFieldName--}
```
public String getFieldName()
```


获取数据源中合并字段的名称。

如果您有从文档字段名称到不同数据源字段名称的映射，那么这就是映射的字段名称。

如果您在文档中指定了字段名称前缀，例如“Image:MyFieldName”，则**FieldName**返回不带前缀的字段名称，即“MyFieldName”。

**退货：**
java.lang.String - 数据源中合并字段的名称。
### getFieldValue() {#getFieldValue--}
```
public Object getFieldValue()
```


从数据源中获取字段的值。此属性包含邮件合并引擎刚刚从您的数据源中为该字段选择的值。您还可以通过设置属性来替换值。

**退货：**
java.lang.Object - 来自数据源的字段值。
### getImage() {#getImage--}
```
public BufferedImage getImage()
```


指定邮件合并引擎必须插入到文档中的图像。

**退货：**
java.awt.image.BufferedImage - 相应的 java.awt.image.BufferedImage 值。
### getImageFileName() {#getImageFileName--}
```
public String getImageFileName()
```


设置邮件合并引擎必须插入到文档中的图像的文件名。

**退货：**
java.lang.String - 邮件合并引擎必须插入到文档中的图像的文件名。
### getImageHeight() {#getImageHeight--}
```
public MergeFieldImageDimension getImageHeight()
```


指定要插入到文档中的图像的图像高度。

该属性的值最初来自模板文档中包含的相应 MERGEFIELD 代码。要覆盖初始值，您应该分配一个实例[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)类为此属性或设置实例的属性[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)类，由此属性返回。

要指示应应用图像高度的原始值，您应该分配**null**此属性的值或设置[MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-)实例的属性[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)此属性返回的类为负值。

**退货：**
[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) - 相应的[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)价值。
### getImageStream() {#getImageStream--}
```
public InputStream getImageStream()
```




**退货：**
java.io.InputStream
### getImageWidth() {#getImageWidth--}
```
public MergeFieldImageDimension getImageWidth()
```


指定要插入到文档中的图像的图像宽度。

该属性的值最初来自模板文档中包含的相应 MERGEFIELD 代码。要覆盖初始值，您应该分配一个实例[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)类为此属性或设置实例的属性[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)类，由此属性返回。

要指示应应用图像宽度的原始值，您应该分配**null**此属性的值或设置[MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-)实例的属性[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)此属性返回的类为负值。

**退货：**
[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) - 相应的[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)价值。
### getRecordIndex() {#getRecordIndex--}
```
public int getRecordIndex()
```


获取正在合并的记录的从零开始的索引。

**退货：**
int - 正在合并的记录的从零开始的索引。
### getShape() {#getShape--}
```
public Shape getShape()
```


指定邮件合并引擎必须插入到文档中的形状。

指定此属性后，邮件合并引擎将忽略所有其他属性，例如[getImageFileName()](../../com.aspose.words/imagefieldmergingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs\#setImageFileName-java.lang.String-)或者**P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream**并简单地将形状插入到文档中。

使用此属性可以完全控制合并图像合并字段的过程。例如，您可以指定[ShapeBase.getWrapType()](../../com.aspose.words/shapebase\#getWrapType--) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase\#setWrapType-int-)或任何其他形状属性以微调结果节点。但是，请注意，您有责任提供形状的内容。

**退货：**
[Shape](../../com.aspose.words/shape) - 相应的[Shape](../../com.aspose.words/shape)价值。
### getTableName() {#getTableName--}
```
public String getTableName()
```


获取当前合并操作的数据表的名称，如果名称不可用，则为空字符串。

**退货：**
java.lang.String - 当前合并操作的数据表名称，如果名称不可用，则为空字符串。
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




### setFieldValue(Object value) {#setFieldValue-java.lang.Object-}
```
public void setFieldValue(Object value)
```


设置来自数据源的字段值。此属性包含邮件合并引擎刚刚从您的数据源中为该字段选择的值。您还可以通过设置属性来替换值。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.Object | 来自数据源的字段值。 |

### setImage(BufferedImage value) {#setImage-java.awt.image.BufferedImage-}
```
public void setImage(BufferedImage value)
```


指定邮件合并引擎必须插入到文档中的图像。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.image.BufferedImage | 对应的java.awt.image.BufferedImage值。 |

### setImageFileName(String value) {#setImageFileName-java.lang.String-}
```
public void setImageFileName(String value)
```


设置邮件合并引擎必须插入到文档中的图像的文件名。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 邮件合并引擎必须插入到文档中的图像的文件名。 |

### setImageHeight(MergeFieldImageDimension value) {#setImageHeight-com.aspose.words.MergeFieldImageDimension-}
```
public void setImageHeight(MergeFieldImageDimension value)
```


指定要插入到文档中的图像的图像高度。

该属性的值最初来自模板文档中包含的相应 MERGEFIELD 代码。要覆盖初始值，您应该分配一个实例[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)类为此属性或设置实例的属性[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)类，由此属性返回。

要指示应应用图像高度的原始值，您应该分配**null**此属性的值或设置[MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-)实例的属性[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)此属性返回的类为负值。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) | 相应的[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)价值。 |

### setImageStream(InputStream value) {#setImageStream-java.io.InputStream-}
```
public void setImageStream(InputStream value)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.io.InputStream |  |

### setImageWidth(MergeFieldImageDimension value) {#setImageWidth-com.aspose.words.MergeFieldImageDimension-}
```
public void setImageWidth(MergeFieldImageDimension value)
```


指定要插入到文档中的图像的图像宽度。

该属性的值最初来自模板文档中包含的相应 MERGEFIELD 代码。要覆盖初始值，您应该分配一个实例[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)类为此属性或设置实例的属性[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)类，由此属性返回。

要指示应应用图像宽度的原始值，您应该分配**null**此属性的值或设置[MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-)实例的属性[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)此属性返回的类为负值。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) | 相应的[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)价值。 |

### setShape(Shape value) {#setShape-com.aspose.words.Shape-}
```
public void setShape(Shape value)
```


指定邮件合并引擎必须插入到文档中的形状。

指定此属性后，邮件合并引擎将忽略所有其他属性，例如[getImageFileName()](../../com.aspose.words/imagefieldmergingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs\#setImageFileName-java.lang.String-)或者**P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream**并简单地将形状插入到文档中。

使用此属性可以完全控制合并图像合并字段的过程。例如，您可以指定[ShapeBase.getWrapType()](../../com.aspose.words/shapebase\#getWrapType--) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase\#setWrapType-int-)或任何其他形状属性以微调结果节点。但是，请注意，您有责任提供形状的内容。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape) | 相应的[Shape](../../com.aspose.words/shape)价值。 |

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
