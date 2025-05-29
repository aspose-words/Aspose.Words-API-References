---
title: PhysicalFontInfo.Version
linktitle: Version
articleTitle: Version
second_title: Aspose.Words for .NET
description: 发现 PhysicalFontInfo 版本属性，轻松访问字体的版本字符串，以增强设计一致性并改进排版。
type: docs
weight: 50
url: /zh/net/aspose.words.fonts/physicalfontinfo/version/
---
## PhysicalFontInfo.Version property

字体的版本字符串。

```csharp
public string Version { get; }
```

## 例子

显示如何列出可用的字体。

```csharp
// 配置 Aspose.Words 从自定义文件夹中获取字体，然后打印每个可用的字体。
FontSourceBase[] folderFontSource = { new FolderFontSource(FontsDir, true) };

foreach (PhysicalFontInfo fontInfo in folderFontSource[0].GetAvailableFonts())
{
    Console.WriteLine("FontFamilyName : {0}", fontInfo.FontFamilyName);
    Console.WriteLine("FullFontName  : {0}", fontInfo.FullFontName);
    Console.WriteLine("Version  : {0}", fontInfo.Version);
    Console.WriteLine("FilePath : {0}\n", fontInfo.FilePath);
}
```

### 也可以看看

* class [PhysicalFontInfo](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
