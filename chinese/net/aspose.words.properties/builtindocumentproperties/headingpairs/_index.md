---
title: BuiltInDocumentProperties.HeadingPairs
linktitle: HeadingPairs
articleTitle: HeadingPairs
second_title: Aspose.Words for .NET
description: 探索 BuiltInDocumentProperties 中的 HeadingPairs 属性，以轻松管理文档标题并增强文档组织。
type: docs
weight: 110
url: /zh/net/aspose.words.properties/builtindocumentproperties/headingpairs/
---
## BuiltInDocumentProperties.HeadingPairs property

指定文档标题及其名称。

```csharp
public object[] HeadingPairs { get; set; }
```

## 评论

每个标题对占据此数组中的两个元素。

该对的第一个元素是String并指定标题名称。 对的第二个元素是Int32并指定此标题的 document 部分的数量[`TitlesOfParts`](../titlesofparts/)财产。

此属性中所有标题对的计数总和必须等于[`TitlesOfParts`](../titlesofparts/)财产。

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
