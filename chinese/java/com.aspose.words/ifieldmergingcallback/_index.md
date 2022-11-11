---
title: I字段MergingCallback
second_title: Aspose.Words for Java API 参考
description:如果您想控制在邮件合并操作期间如何将数据插入到合并字段中，请实现此接口。
type: docs
weight: 641
url: /zh/java/com.aspose.words/ifieldmergingcallback/
---
```
public interface I字段MergingCallback
```

如果您想控制在邮件合并操作期间如何将数据插入到合并字段中，请实现此接口。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [fieldMerging(字段MergingArgs args)](#fieldMerging-com.aspose.words.字段MergingArgs-) | 当 Aspose.Words 邮件合并引擎即将将数据插入文档中的合并字段时调用。 |
| [image字段Merging(Image字段MergingArgs args)](#image字段Merging-com.aspose.words.Image字段MergingArgs-) | 当 Aspose.Words 邮件合并引擎将图像插入合并字段时调用。 |
### fieldMerging(字段MergingArgs args) {#fieldMerging-com.aspose.words.字段MergingArgs-}
```
public abstract void fieldMerging(字段MergingArgs args)
```


当 Aspose.Words 邮件合并引擎即将将数据插入文档中的合并字段时调用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [字段MergingArgs](../../com.aspose.words/fieldmergingargs) |  |

### image字段Merging(Image字段MergingArgs args) {#image字段Merging-com.aspose.words.Image字段MergingArgs-}
```
public abstract void image字段Merging(Image字段MergingArgs args)
```


当 Aspose.Words 邮件合并引擎将图像插入合并字段时调用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [Image字段MergingArgs](../../com.aspose.words/imagefieldmergingargs) |  |
