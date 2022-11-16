---
title: IResourceSavingCallback
second_title: Aspose.Words for Java API 参考
description: 如果你想控制Aspose.Words在保存文档到固定页面HTML或SVG时如何保存外部资源图像字体和css，实现这个接口。
type: docs
weight: 657
url: /zh/java/com.aspose.words/iresourcesavingcallback/
---
```
public interface IResourceSavingCallback
```

如果您想在将文档保存为固定页面 HTML 或 SVG 时控制 Aspose.Words 如何保存外部资源（图像、字体和 css），请实现此接口。
## 方法

| 方法 | 描述 |
| --- | --- |
| [resourceSaving(ResourceSavingArgs args)](#resourceSaving-com.aspose.words.ResourceSavingArgs-) | 当 Aspose.Words 将外部资源保存为固定页面 HTML 或 SVG 格式时调用。 |
### resourceSaving(ResourceSavingArgs args) {#resourceSaving-com.aspose.words.ResourceSavingArgs-}
```
public abstract void resourceSaving(ResourceSavingArgs args)
```


当 Aspose.Words 将外部资源保存为固定页面 HTML 或 SVG 格式时调用。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [ResourceSavingArgs](../../com.aspose.words/resourcesavingargs) |  |
