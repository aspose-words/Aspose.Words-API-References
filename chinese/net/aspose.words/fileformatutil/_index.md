---
title: FileFormatUtil Class
linktitle: FileFormatUtil
articleTitle: FileFormatUtil
second_title: Aspose.Words for .NET
description: 使用 Aspose.Words.FileFormatUtil 轻松管理文件格式。检测格式并无缝转换扩展名，从而提高工作效率。
type: docs
weight: 3230
url: /zh/net/aspose.words/fileformatutil/
---
## FileFormatUtil class

提供处理文件格式的实用方法，例如检测文件格式 或将文件扩展名转换为/从文件格式枚举。

要了解更多信息，请访问[检测文件格式并检查格式兼容性](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/)文档文章。

```csharp
public static class FileFormatUtil
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| static [ContentTypeToLoadFormat](../../aspose.words/fileformatutil/contenttypetoloadformat/)(*string*) | 将 IANA 内容类型转换为加载格式枚举值。 |
| static [ContentTypeToSaveFormat](../../aspose.words/fileformatutil/contenttypetosaveformat/)(*string*) | 将 IANA 内容类型转换为保存格式枚举值。 |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat)(*Stream*) | 检测并返回有关存储在流中的文档格式的信息。 |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat_1)(*string*) | 检测并返回有关存储在磁盘文件中的文档格式的信息。 |
| static [ExtensionToSaveFormat](../../aspose.words/fileformatutil/extensiontosaveformat/)(*string*) | 将文件扩展名转换为[`SaveFormat`](../saveformat/)值. |
| static [ImageTypeToExtension](../../aspose.words/fileformatutil/imagetypetoextension/)(*[ImageType](../../aspose.words.drawing/imagetype/)*) | 将 Aspose.Words 图像类型枚举值转换为文件扩展名。返回的扩展名是一个以点开头的小写字符串。 |
| static [LoadFormatToExtension](../../aspose.words/fileformatutil/loadformattoextension/)(*[LoadFormat](../loadformat/)*) | 将加载格式枚举值转换为文件扩展名。返回的扩展名是一个以点开头的小写字符串。 |
| static [LoadFormatToSaveFormat](../../aspose.words/fileformatutil/loadformattosaveformat/)(*[LoadFormat](../loadformat/)*) | 转换[`LoadFormat`](../loadformat/)价值[`SaveFormat`](../saveformat/)如果可能的话，值。 |
| static [SaveFormatToExtension](../../aspose.words/fileformatutil/saveformattoextension/)(*[SaveFormat](../saveformat/)*) | 将保存格式枚举值转换为文件扩展名。返回的扩展名是一个以点开头的小写字符串。 |
| static [SaveFormatToLoadFormat](../../aspose.words/fileformatutil/saveformattoloadformat/)(*[SaveFormat](../saveformat/)*) | 转换[`SaveFormat`](../saveformat/)价值[`LoadFormat`](../loadformat/)如果可能的话，值。 |

## 例子

展示如何检测 html 文件中的编码。

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// 仅当我们为 html 文档创建 FileFormatInfo 对象时才使用 Encoding 属性。
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
