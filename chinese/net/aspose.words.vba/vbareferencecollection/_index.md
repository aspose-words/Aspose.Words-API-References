---
title: VbaReferenceCollection Class
linktitle: VbaReferenceCollection
articleTitle: VbaReferenceCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Vba.VbaReferenceCollection 类，这是一个用于在项目中有效管理 VbaReference 对象的强大工具。
type: docs
weight: 7450
url: /zh/net/aspose.words.vba/vbareferencecollection/
---
## VbaReferenceCollection class

代表[`VbaReference`](../vbareference/)对象.

要了解更多信息，请访问[使用 VBA 宏](https://docs.aspose.com/words/net/working-with-vba-macros/)文档文章。

```csharp
public sealed class VbaReferenceCollection : IEnumerable<VbaReference>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.vba/vbareferencecollection/count/) { get; } | 返回集合中的 VBA 引用数。 |
| [Item](../../aspose.words.vba/vbareferencecollection/item/) { get; } | 获取[`VbaReference`](../vbareference/)指定索引处的对象。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Remove](../../aspose.words.vba/vbareferencecollection/remove/)(*[VbaReference](../vbareference/)*) | 删除指定的第一次出现[`VbaReference`](../vbareference/)来自该系列的物品。 |
| [RemoveAt](../../aspose.words.vba/vbareferencecollection/removeat/)(*int*) | 删除[`VbaReference`](../vbareference/)集合中指定索引处的元素。 |

## 例子

展示如何从 VBA 参考集合中获取/删除元素。

```csharp
public void RemoveVbaReference()
{
    const string brokenPath = @"X:\broken.dll";
    Document doc = new Document(MyDir + "VBA project.docm");

    VbaReferenceCollection references = doc.VbaProject.References;
    Assert.AreEqual(5 ,references.Count);

    for (int i = references.Count - 1; i >= 0; i--)
    {
        VbaReference reference = doc.VbaProject.References[i];
        string path = GetLibIdPath(reference);

        if (path == brokenPath)
            references.RemoveAt(i);
    }
    Assert.AreEqual(4 ,references.Count);

    references.Remove(references[1]);
    Assert.AreEqual(3 ,references.Count);

    doc.Save(ArtifactsDir + "VbaProject.RemoveVbaReference.docm"); 
}

/// <summary>
 /// 返回表示指定引用的 LibId 路径的字符串。
/// </summary>
private static string GetLibIdPath(VbaReference reference)
{
    switch (reference.Type)
    {
        case VbaReferenceType.Registered:
        case VbaReferenceType.Original:
        case VbaReferenceType.Control:
            return GetLibIdReferencePath(reference.LibId);
        case VbaReferenceType.Project:
            return GetLibIdProjectPath(reference.LibId);
        default:
            throw new ArgumentOutOfRangeException();
    }
}

/// <summary>
/// 从自动化类型库的指定标识符返回路径。
/// </summary>
private static string GetLibIdReferencePath(string libIdReference)
{
    if (libIdReference != null)
    {
        string[] refParts = libIdReference.Split('#');
        if (refParts.Length > 3)
            return refParts[3];
    }

    return "";
}

/// <summary>
/// 从自动化类型库的指定标识符返回路径。
/// </summary>
private static string GetLibIdProjectPath(string libIdProject)
{
    return libIdProject != null ? libIdProject.Substring(3) : "";
}
```

### 也可以看看

* class [VbaReference](../vbareference/)
* 命名空间 [Aspose.Words.Vba](../../aspose.words.vba/)
* 部件 [Aspose.Words](../../)
