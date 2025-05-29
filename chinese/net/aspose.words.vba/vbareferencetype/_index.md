---
title: VbaReferenceType Enum
linktitle: VbaReferenceType
articleTitle: VbaReferenceType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Vba.VbaReferenceType 枚举以轻松定义 VbaReference 对象类型，增强文档自动化和管理。
type: docs
weight: 7460
url: /zh/net/aspose.words.vba/vbareferencetype/
---
## VbaReferenceType enumeration

允许指定[`VbaReference`](../vbareference/)对象.

```csharp
public enum VbaReferenceType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Registered | `13` | 指定自动化类型库引用类型。 |
| Project | `14` | 指定了外部 VBA 项目引用类型。 |
| Original | `51` | 指定原始自动化类型库引用类型。 |
| Control | `47` | 指定一个旋转类型库引用类型。 |

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
