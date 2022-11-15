---
title: IReplacingCallback
second_title: Aspose.Words for Java API 参考
description: 如果您想在查找和替换操作期间调用自己的自定义方法，请实现此接口。
type: docs
weight: 655
url: /zh/java/com.aspose.words/ireplacingcallback/
---
```
public interface IReplacingCallback
```

如果您想在查找和替换操作期间调用自己的自定义方法，请实现此接口。
## 方法

| 方法 | 描述 |
| --- | --- |
| [replacing(ReplacingArgs args)](#replacing-com.aspose.words.ReplacingArgs-) | 用户定义的方法，在替换操作期间为在替换之前找到的每个匹配项调用。 |
### replacing(ReplacingArgs args) {#replacing-com.aspose.words.ReplacingArgs-}
```
public abstract int replacing(ReplacingArgs args)
```


用户定义的方法，在替换操作期间为在替换之前找到的每个匹配项调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [ReplacingArgs](../../com.aspose.words/replacingargs) |  |

**退货：**
诠释 - A[ReplaceAction](../../com.aspose.words/replaceaction)指定要对当前匹配项采取的操作的值。返回值是其中之一[ReplaceAction](../../com.aspose.words/replaceaction)常数。