---
title: IWarningCallback
second_title: Aspose.Words for Java API 参考
description: 如果您希望调用自己的自定义方法来捕获在文档加载或保存期间可能发生的保真度丢失警告，请实现此接口。
type: docs
weight: 661
url: /zh/java/com.aspose.words/iwarningcallback/
---
```
public interface IWarningCallback
```

如果您希望调用自己的自定义方法来捕获在文档加载或保存期间可能发生的保真度丢失警告，请实现此接口。
## 方法

| 方法 | 描述 |
| --- | --- |
| [warning(WarningInfo info)](#warning-com.aspose.words.WarningInfo-) | Aspose.Words 在文档加载或保存过程中遇到可能导致格式丢失或数据保真度丢失的问题时调用此方法。 |
### warning(WarningInfo info) {#warning-com.aspose.words.WarningInfo-}
```
public abstract void warning(WarningInfo info)
```


Aspose.Words 在文档加载或保存过程中遇到可能导致格式丢失或数据保真度丢失的问题时调用此方法。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| info | [WarningInfo](../../com.aspose.words/warninginfo) |  |
