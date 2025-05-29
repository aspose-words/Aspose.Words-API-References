---
title: FontSourceBase.GetAvailableFonts
linktitle: GetAvailableFonts
articleTitle: GetAvailableFonts
second_title: Aspose.Words for .NET
description: 使用 FontSourceBase 的 GetAvailableFonts 方法发现可用的字体。丰富多样的高质量字体选择，助您项目锦上添花！
type: docs
weight: 40
url: /zh/net/aspose.words.fonts/fontsourcebase/getavailablefonts/
---
## FontSourceBase.GetAvailableFonts method

返回可通过此源使用的字体列表。

```csharp
public IList<PhysicalFontInfo> GetAvailableFonts()
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

* class [PhysicalFontInfo](../../physicalfontinfo/)
* class [FontSourceBase](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
