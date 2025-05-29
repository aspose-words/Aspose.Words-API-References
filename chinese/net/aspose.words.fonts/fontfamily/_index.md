---
title: FontFamily Enum
linktitle: FontFamily
articleTitle: FontFamily
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fonts.FontFamily 枚举——轻松管理不同字体系列以增强文档样式和格式的关键。
type: docs
weight: 3340
url: /zh/net/aspose.words.fonts/fontfamily/
---
## FontFamily enumeration

代表字体系列。

```csharp
public enum FontFamily
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Auto | `0` | 指定通用字体系列名称。当字体 的信息不存在或无关紧要时，使用此名称。系统将使用默认字体。 |
| Roman | `1` | 指定带衬线的比例字体。例如 Times New Roman。 |
| Swiss | `2` | 指定无衬线的比例字体。例如 Arial。 |
| Modern | `3` | 指定带或不带衬线的等宽字体。等宽字体通常比较现代；例如 Pica、Elite 和 Courier New。 |
| Script | `4` | 指定设计为看起来像手写的字体；示例包括 Script 和 Cursive。 |
| Decorative | `5` | 指定一种新字体。例如古英语。 |

## 评论

字体系列是一组具有共同笔画宽度和衬线特征的字体。

## 例子

展示如何访问和打印文档中每种字体的详细信息。

```csharp
Document doc = new Document(MyDir + "Document.docx");

IEnumerator<FontInfo> fontCollectionEnumerator = doc.FontInfos.GetEnumerator();
while (fontCollectionEnumerator.MoveNext())
{
    FontInfo fontInfo = fontCollectionEnumerator.Current;
    if (fontInfo != null)
    {
        Console.WriteLine("Font name: " + fontInfo.Name);

        // Alt 名称通常为空白。
        Console.WriteLine("Alt name: " + fontInfo.AltName);
        Console.WriteLine("\t- Family: " + fontInfo.Family);
        Console.WriteLine("\t- " + (fontInfo.IsTrueType ? "Is TrueType" : "Is not TrueType"));
        Console.WriteLine("\t- Pitch: " + fontInfo.Pitch);
        Console.WriteLine("\t- Charset: " + fontInfo.Charset);
        Console.WriteLine("\t- Panose:");
        Console.WriteLine("\t\tFamily Kind: " + fontInfo.Panose[0]);
        Console.WriteLine("\t\tSerif Style: " + fontInfo.Panose[1]);
        Console.WriteLine("\t\tWeight: " + fontInfo.Panose[2]);
        Console.WriteLine("\t\tProportion: " + fontInfo.Panose[3]);
        Console.WriteLine("\t\tContrast: " + fontInfo.Panose[4]);
        Console.WriteLine("\t\tStroke Variation: " + fontInfo.Panose[5]);
        Console.WriteLine("\t\tArm Style: " + fontInfo.Panose[6]);
        Console.WriteLine("\t\tLetterform: " + fontInfo.Panose[7]);
        Console.WriteLine("\t\tMidline: " + fontInfo.Panose[8]);
        Console.WriteLine("\t\tX-Height: " + fontInfo.Panose[9]);
    }
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)
