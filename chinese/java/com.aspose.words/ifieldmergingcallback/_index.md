---
title: IFieldMergingCallback
second_title: Aspose.Words for Java API 参考
description: 如果要控制在邮件合并操作期间如何将数据插入合并字段，请实现此接口。
type: docs
weight: 641
url: /zh/java/com.aspose.words/ifieldmergingcallback/
---
```
public interface IFieldMergingCallback
```

如果要控制在邮件合并操作期间如何将数据插入合并字段，请实现此接口。
## 方法

| 方法 | 描述 |
| --- | --- |
| [fieldMerging(FieldMergingArgs args)](#fieldMerging-com.aspose.words.FieldMergingArgs-) | 当 Aspose.Words 邮件合并引擎即将向文档中的合并字段插入数据时调用。 |
| [imageFieldMerging(ImageFieldMergingArgs args)](#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs-) | 当 Aspose.Words 邮件合并引擎准备将图像插入合并字段时调用。 |
### fieldMerging(FieldMergingArgs args) {#fieldMerging-com.aspose.words.FieldMergingArgs-}
```
public abstract void fieldMerging(FieldMergingArgs args)
```


当 Aspose.Words 邮件合并引擎即将向文档中的合并字段插入数据时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [FieldMergingArgs](../../com.aspose.words/fieldmergingargs) |  |

### imageFieldMerging(ImageFieldMergingArgs args) {#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs-}
```
public abstract void imageFieldMerging(ImageFieldMergingArgs args)
```


当 Aspose.Words 邮件合并引擎准备将图像插入合并字段时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [ImageFieldMergingArgs](../../com.aspose.words/imagefieldmergingargs) |  |
