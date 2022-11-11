---
title: IResourceLoadingCallback
second_title: Aspose.Words for Java API 参考
description:如果您想控制 Aspose.Words 在导入文档和使用 .
type: docs
weight: 656
url: /zh/java/com.aspose.words/iresourceloadingcallback/
---
```
public interface IResourceLoadingCallback
```

如果您想控制 Aspose.Words 在导入文档和插入图像时如何加载外部资源，请实现此接口[DocumentBuilder](../../com.aspose.words/documentbuilder).
## 方法s

| 方法 | 描述 |
| --- | --- |
| [resourceLoading(ResourceLoadingArgs args)](#resourceLoading-com.aspose.words.ResourceLoadingArgs-) | 当 Aspose.Words 加载任何外部资源时调用。 |
### resourceLoading(ResourceLoadingArgs args) {#resourceLoading-com.aspose.words.ResourceLoadingArgs-}
```
public abstract int resourceLoading(ResourceLoadingArgs args)
```


当 Aspose.Words 加载任何外部资源时调用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [ResourceLoadingArgs](../../com.aspose.words/resourceloadingargs) |  |

**退货:**
整数