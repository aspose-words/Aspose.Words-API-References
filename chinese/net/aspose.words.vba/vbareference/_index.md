---
title: VbaReference Class
linktitle: VbaReference
articleTitle: VbaReference
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Vba.VbaReference 类，实现与自动化类型库和 VBA 项目的无缝集成。立即增强您的文档自动化！
type: docs
weight: 7440
url: /zh/net/aspose.words.vba/vbareference/
---
## VbaReference class

实现对自动化类型库或 VBA 项目的引用。

要了解更多信息，请访问[使用 VBA 宏](https://docs.aspose.com/words/net/working-with-vba-macros/)文档文章。

```csharp
public abstract class VbaReference
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| abstract [LibId](../../aspose.words.vba/vbareference/libid/) { get; } | 获取包含自动化类型库标识符的字符串值。 |
| abstract [Type](../../aspose.words.vba/vbareference/type/) { get; } | 获取[`VbaReferenceType`](../vbareferencetype/)指示引用类型的对象`VbaReference`对象代表. |

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

* 命名空间 [Aspose.Words.Vba](../../aspose.words.vba/)
* 部件 [Aspose.Words](../../)
