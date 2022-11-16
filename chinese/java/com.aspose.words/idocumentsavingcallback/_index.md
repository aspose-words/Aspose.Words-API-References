---
title: IDocumentSavingCallback
second_title: Aspose.Words for Java API 参考
description: 如果您希望在保存文档期间调用自己的自定义方法，请实现此接口。
type: docs
weight: 639
url: /zh/java/com.aspose.words/idocumentsavingcallback/
---
```
public interface IDocumentSavingCallback
```

如果您希望在保存文档期间调用自己的自定义方法，请实现此接口。
## 方法

| 方法 | 描述 |
| --- | --- |
| [notify(DocumentSavingArgs args)](#notify-com.aspose.words.DocumentSavingArgs-) | 调用它来通知文档保存进度。 |
### notify(DocumentSavingArgs args) {#notify-com.aspose.words.DocumentSavingArgs-}
```
public abstract void notify(DocumentSavingArgs args)
```


调用它来通知文档保存进度。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [DocumentSavingArgs](../../com.aspose.words/documentsavingargs) | 事件的一个参数。此接口的主要用途是允许应用程序代码获取进度状态和中止保存过程。

异常应该从堕胎的进度回调中抛出，并且应该在消费者代码中捕获。|
