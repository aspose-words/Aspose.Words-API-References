---
title: IImageSavingCallback
second_title: Aspose.Words for Java API Reference
description: 如果您想控制 Aspose.Words 在将文档保存为 HTML 时如何保存图像，请实现此接口。
type: docs
weight: 648
url: /zh/java/com.aspose.words/iimagesavingcallback/
---
```
public interface IImageSavingCallback
```

如果您想控制 Aspose.Words 在将文档保存为 HTML 时如何保存图像，请实现此接口。可以被其他格式使用。
## 方法

| 方法 | 描述 |
| --- | --- |
| [imageSaving(ImageSavingArgs args)](#imageSaving-com.aspose.words.ImageSavingArgs-) | 当 Aspose.Words 将图像保存到 HTML 时调用。 |
### imageSaving(ImageSavingArgs args) {#imageSaving-com.aspose.words.ImageSavingArgs-}
```
public abstract void imageSaving(ImageSavingArgs args)
```


当 Aspose.Words 将图像保存到 HTML 时调用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| args | [ImageSavingArgs](../../com.aspose.words/imagesavingargs) |  |
