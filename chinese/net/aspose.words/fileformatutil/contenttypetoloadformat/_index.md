---
title: FileFormatUtil.ContentTypeToLoadFormat
linktitle: ContentTypeToLoadFormat
articleTitle: ContentTypeToLoadFormat
second_title: Aspose.Words for .NET
description: 使用 FileFormatUtil ContentTypeToLoadFormat 方法，轻松将 IANA 内容类型转换为加载格式值。立即简化您的文件处理！
type: docs
weight: 10
url: /zh/net/aspose.words/fileformatutil/contenttypetoloadformat/
---
## FileFormatUtil.ContentTypeToLoadFormat method

将 IANA 内容类型转换为加载格式枚举值。

```csharp
public static LoadFormat ContentTypeToLoadFormat(string contentType)
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentException | 无法转换时抛出。 |

## 例子

展示如何从每个媒体类型字符串中找到相应的 Aspose 加载/保存格式。

```csharp
 // ContentTypeToSaveFormat/ContentTypeToLoadFormat 方法仅接受官方 IANA 媒体类型名称，也称为 MIME 类型。
// 所有有效的媒体类型都列在这里：https://www.iana.org/assignments/media-types/media-types.xhtml。

// 尝试将 SaveFormat 与部分媒体类型字符串关联起来是行不通的。
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("jpeg"));

// 如果 Aspose.Words 没有与内容类型对应的保存/加载格式，也会引发异常。
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("application/zip"));

// 可以保存下面列出的文件类型，但不能使用 Aspose.Words 加载。
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToLoadFormat("image/jpeg"));

Assert.AreEqual(SaveFormat.Jpeg, FileFormatUtil.ContentTypeToSaveFormat("image/jpeg"));
Assert.AreEqual(SaveFormat.Png, FileFormatUtil.ContentTypeToSaveFormat("image/png"));
Assert.AreEqual(SaveFormat.Tiff, FileFormatUtil.ContentTypeToSaveFormat("image/tiff"));
Assert.AreEqual(SaveFormat.Gif, FileFormatUtil.ContentTypeToSaveFormat("image/gif"));
Assert.AreEqual(SaveFormat.Emf, FileFormatUtil.ContentTypeToSaveFormat("image/x-emf"));
Assert.AreEqual(SaveFormat.Xps, FileFormatUtil.ContentTypeToSaveFormat("application/vnd.ms-xpsdocument"));
Assert.AreEqual(SaveFormat.Pdf, FileFormatUtil.ContentTypeToSaveFormat("application/pdf"));
Assert.AreEqual(SaveFormat.Svg, FileFormatUtil.ContentTypeToSaveFormat("image/svg+xml"));
Assert.AreEqual(SaveFormat.Epub, FileFormatUtil.ContentTypeToSaveFormat("application/epub+zip"));

// 对于可以保存和加载的文件类型，我们可以将媒体类型与加载格式和保存格式进行匹配。
Assert.AreEqual(LoadFormat.Doc, FileFormatUtil.ContentTypeToLoadFormat("application/msword"));
Assert.AreEqual(SaveFormat.Doc, FileFormatUtil.ContentTypeToSaveFormat("application/msword"));

Assert.AreEqual(LoadFormat.Docx,
    FileFormatUtil.ContentTypeToLoadFormat(
        "application/vnd.openxmlformats-officedocument.wordprocessingml.document"));
Assert.AreEqual(SaveFormat.Docx,
    FileFormatUtil.ContentTypeToSaveFormat(
        "application/vnd.openxmlformats-officedocument.wordprocessingml.document"));

Assert.AreEqual(LoadFormat.Text, FileFormatUtil.ContentTypeToLoadFormat("text/plain"));
Assert.AreEqual(SaveFormat.Text, FileFormatUtil.ContentTypeToSaveFormat("text/plain"));

Assert.AreEqual(LoadFormat.Rtf, FileFormatUtil.ContentTypeToLoadFormat("application/rtf"));
Assert.AreEqual(SaveFormat.Rtf, FileFormatUtil.ContentTypeToSaveFormat("application/rtf"));

Assert.AreEqual(LoadFormat.Html, FileFormatUtil.ContentTypeToLoadFormat("text/html"));
Assert.AreEqual(SaveFormat.Html, FileFormatUtil.ContentTypeToSaveFormat("text/html"));

Assert.AreEqual(LoadFormat.Mhtml, FileFormatUtil.ContentTypeToLoadFormat("multipart/related"));
Assert.AreEqual(SaveFormat.Mhtml, FileFormatUtil.ContentTypeToSaveFormat("multipart/related"));
```

### 也可以看看

* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
