---
title: FontInfoCollection.GetEnumerator
second_title: Aspose.Words for .NET API 参考
description: FontInfoCollection 方法. 返回一个可用于迭代集合中所有项目的枚举器对象
type: docs
weight: 70
url: /zh/net/aspose.words.fonts/fontinfocollection/getenumerator/
---
## FontInfoCollection.GetEnumerator method

返回一个可用于迭代集合中所有项目的枚举器对象。

```csharp
public IEnumerator<FontInfo> GetEnumerator()
```

### 例子

显示如何访问和打印文档中每种字体的详细信息。

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

* class [FontInfo](../../fontinfo/)
* class [FontInfoCollection](../)
* 命名空间 [Aspose.Words.Fonts](../../fontinfocollection/)
* 部件 [Aspose.Words](../../../)


