---
title: PhysicalFontInfo.Version
second_title: Aspose.Words for .NET API 参考
description: PhysicalFontInfo 财产. 字体的版本字符串
type: docs
weight: 40
url: /zh/net/aspose.words.fonts/physicalfontinfo/version/
---
## PhysicalFontInfo.Version property

字体的版本字符串。

```csharp
public string Version { get; }
```

### 例子

演示如何列出可用字体。

```csharp
// 将 Aspose.Words 配置为从自定义文件夹获取字体，然后打印每种可用字体。
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
* 命名空间 [Aspose.Words.Fonts](../../physicalfontinfo/)
* 部件 [Aspose.Words](../../../)


