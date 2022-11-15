---
title: IPageLayoutCallback
second_title: Aspose.Words for Java API 参考
description: 如果您希望在构建和呈现页面布局模型期间调用自己的自定义方法，请实现此接口。
type: docs
weight: 653
url: /zh/java/com.aspose.words/ipagelayoutcallback/
---
```
public interface IPageLayoutCallback
```

如果您希望在构建和呈现页面布局模型期间调用自己的自定义方法，请实现此接口。此接口的主要用途是允许应用程序代码中止构建过程。

可以在文档开始时仅为几页构建页面布局模型，然后中止进程并仅呈现已经构建的内容。

但是请注意，如果进程完成，渲染结果可能与每个页面的渲染结果不匹配。

此技术可能不适用于每个文档，或者可能完全失败。
## 方法

| 方法 | 描述 |
| --- | --- |
| [notify(PageLayoutCallbackArgs args)](#notify-com.aspose.words.PageLayoutCallbackArgs-) | 这被调用来通知布局构建和渲染进度。 |
### notify(PageLayoutCallbackArgs args) {#notify-com.aspose.words.PageLayoutCallbackArgs-}
```
public abstract void notify(PageLayoutCallbackArgs args)
```


这被调用来通知布局构建和渲染进度。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [PageLayoutCallbackArgs](../../com.aspose.words/pagelayoutcallbackargs) | 事件的论据。实现中止布局构建过程时抛出异常。 |
