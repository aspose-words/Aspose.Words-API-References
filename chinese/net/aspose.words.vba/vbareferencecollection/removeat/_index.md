---
title: VbaReferenceCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words for .NET
description: 使用 RemoveAt 方法轻松管理您的 VbaReferenceCollection，通过索引删除元素，提高您的 VBA 编码效率。
type: docs
weight: 40
url: /zh/net/aspose.words.vba/vbareferencecollection/removeat/
---
## VbaReferenceCollection.RemoveAt method

删除[`VbaReference`](../../vbareference/)集合中指定索引处的元素。

```csharp
public void RemoveAt(int index)
```

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

* class [VbaReferenceCollection](../)
* 命名空间 [Aspose.Words.Vba](../../../aspose.words.vba/)
* 部件 [Aspose.Words](../../../)
