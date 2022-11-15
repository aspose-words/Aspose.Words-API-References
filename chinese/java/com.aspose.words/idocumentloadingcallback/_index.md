---
title: IDocumentLoadingCallback
second_title: Aspose.Words for Java API 参考
description: 如果您想在加载文档期间调用自己的自定义方法，请实现此接口。
type: docs
weight: 636
url: /zh/java/com.aspose.words/idocumentloadingcallback/
---
```
public interface IDocumentLoadingCallback
```

如果您想在加载文档期间调用自己的自定义方法，请实现此接口。
## 方法

| 方法 | 描述 |
| --- | --- |
| [notify(DocumentLoadingArgs args)](#notify-com.aspose.words.DocumentLoadingArgs-) | 这被调用以通知文档加载进度。 |
### notify(DocumentLoadingArgs args) {#notify-com.aspose.words.DocumentLoadingArgs-}
```
public abstract void notify(DocumentLoadingArgs args)
```


这被调用以通知文档加载进度。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [DocumentLoadingArgs](../../com.aspose.words/documentloadingargs) | 事件的一个参数。此接口的主要用途是允许应用程序代码获取进度状态和中止加载过程。

异常应该从堕胎的进度回调中抛出，并且应该在消费者代码中捕获。|
