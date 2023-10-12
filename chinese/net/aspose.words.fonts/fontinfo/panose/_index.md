---
title: FontInfo.Panose
second_title: Aspose.Words for .NET API 参考
description: FontInfo 财产. 获取或设置 PANOSE 字体分类号
type: docs
weight: 60
url: /zh/net/aspose.words.fonts/fontinfo/panose/
---
## FontInfo.Panose property

获取或设置 PANOSE 字体分类号。

```csharp
public byte[] Panose { get; set; }
```

### 评论

PANOSE 是对字体关键视觉特征 （例如对比度、粗细和衬线样式）的紧凑 10 字节描述。这些数字代表系列种类、衬线样式、 粗细、比例、对比度、笔画变化、臂样式、字母形式、中线和 X 高度。

可`无效的`。

### 例子

演示如何访问和打印文档中每种字体的详细信息。

```csharp
Document doc = new Document(MyDir + "Document.docx");

IEnumerator<FontInfo> fontCollectionEnumerator = doc.FontInfos.GetEnumerator();
while (fontCollectionEnumerator.MoveNext())
{
    FontInfo fontInfo = fontCollectionEnumerator.Current;
    if (fontInfo != null)
    {
        Console.WriteLine("Font name: " + fontInfo.Name);

        // Alt 名称通常为空。
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

* class [FontInfo](../)
* 命名空间 [Aspose.Words.Fonts](../../fontinfo/)
* 部件 [Aspose.Words](../../../)


