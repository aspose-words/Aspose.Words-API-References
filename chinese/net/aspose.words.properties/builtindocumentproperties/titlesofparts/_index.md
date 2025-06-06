---
title: BuiltInDocumentProperties.TitlesOfParts
linktitle: TitlesOfParts
articleTitle: TitlesOfParts
second_title: Aspose.Words for .NET
description: 探索 BuiltInDocumentProperties 中的 TitlesOfParts 属性。使用清晰、可自定义的各部分名称，轻松管理文档各部分，从而增强组织性。
type: docs
weight: 330
url: /zh/net/aspose.words.properties/builtindocumentproperties/titlesofparts/
---
## BuiltInDocumentProperties.TitlesOfParts property

数组中的每个字符串指定文档中某个部分的名称。

```csharp
public string[] TitlesOfParts { get; set; }
```

## 评论

Aspose.Words 不会更新此属性。

## 例子

显示“HeadingPairs”和“TitlesOfParts”属性之间的关系。

```csharp
Document doc = new Document(MyDir + "Heading pairs and titles of parts.docx");

// 我们可以通过以下方式找到这些集合的组合值
//“文件”->“属性”->“高级属性”->“内容”选项卡。
// HeadingPairs 属性是 <string, int> 对的集合，
// 确定标题跨越多少个文档部分。
object[] headingPairs = doc.BuiltInDocumentProperties.HeadingPairs;

// TitlesOfParts 属性包含属于上述标题的部分的名称。
string[] titlesOfParts = doc.BuiltInDocumentProperties.TitlesOfParts;

int headingPairsIndex = 0;
int titlesOfPartsIndex = 0;
while (headingPairsIndex < headingPairs.Length)
{
    Console.WriteLine($"Parts for {headingPairs[headingPairsIndex++]}:");
    int partsCount = Convert.ToInt32(headingPairs[headingPairsIndex++]);

    for (int i = 0; i < partsCount; i++)
        Console.WriteLine($"\t\"{titlesOfParts[titlesOfPartsIndex++]}\"");
}
```

### 也可以看看

* class [BuiltInDocumentProperties](../)
* 命名空间 [Aspose.Words.Properties](../../../aspose.words.properties/)
* 部件 [Aspose.Words](../../../)
