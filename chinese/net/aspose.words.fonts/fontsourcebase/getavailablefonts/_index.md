---
title: FontSourceBase.GetAvailableFonts
second_title: Aspose.Words for .NET API 参考
description: FontSourceBase 方法. 返回通过此源可用的字体列表
type: docs
weight: 40
url: /zh/net/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase.GetAvailableFonts method

返回通过此源可用的字体列表。

```csharp
public IList<PhysicalFontInfo> GetAvailableFonts()
```

### 例子

显示如何列出可用字体。

```csharp
// 将 Aspose.Words 配置为从自定义文件夹获取字体，然后打印所有可用字体。
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

* class [PhysicalFontInfo](../../physicalfontinfo/)
* class [FontSourceBase](../)
* 命名空间 [Aspose.Words.Fonts](../../fontsourcebase/)
* 部件 [Aspose.Words](../../../)


