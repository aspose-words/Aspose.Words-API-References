---
title: PhysicalFontInfo.FilePath
second_title: Aspose.Words for .NET API 参考
description: PhysicalFontInfo 财产. 字体文件的路径如果有
type: docs
weight: 10
url: /zh/net/aspose.words.fonts/physicalfontinfo/filepath/
---
## PhysicalFontInfo.FilePath property

字体文件的路径（如果有）。

```csharp
public string FilePath { get; }
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


