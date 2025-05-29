---
title: Document.PackageCustomParts
linktitle: PackageCustomParts
articleTitle: PackageCustomParts
second_title: Aspose.Words for .NET
description: 轻松管理 OOXML 包中的自定义部分。轻松访问和修改链接内容，增强文档的灵活性和功能性。
type: docs
weight: 320
url: /zh/net/aspose.words/document/packagecustomparts/
---
## Document.PackageCustomParts property

获取或设置使用“未知关系”链接到 OOXML 包的自定义部分（任意内容）的集合。

```csharp
public CustomPartCollection PackageCustomParts { get; set; }
```

## 评论

请勿将这些自定义部分与自定义 XML 数据混淆。如果您需要访问自定义 XML 部分，请使用[`CustomXmlParts`](../customxmlparts/)财产。

此集合包含 OOXML 部分，其父级是 OOXML 包，并且它们的目标是“未知关系”。 有关详细信息，请参阅[`CustomPart`](../../../aspose.words.markup/custompart/)。

Aspose.Words 仅将自定义部分加载并保存到 OOXML 文档中。

此属性不能`无效的`。

## 例子

展示如何访问文档的任意自定义部分集合。

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// 克隆第二部分，然后将克隆添加到集合中。
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// 枚举集合并打印每个部分。
using (IEnumerator<CustomPart> enumerator = doc.PackageCustomParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Part index {index}:");
        Console.WriteLine($"\tName:\t\t\t\t{enumerator.Current.Name}");
        Console.WriteLine($"\tContent type:\t\t{enumerator.Current.ContentType}");
        Console.WriteLine($"\tRelationship type:\t{enumerator.Current.RelationshipType}");
        Console.WriteLine(enumerator.Current.IsExternal ?
            "\tSourced from outside the document" :
            $"\tStored within the document, length: {enumerator.Current.Data.Length} bytes");
        index++;
    }
}

// 我们可以从该集合中单独删除元素，也可以一次性删除所有元素。
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### 也可以看看

* class [CustomPartCollection](../../../aspose.words.markup/custompartcollection/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
