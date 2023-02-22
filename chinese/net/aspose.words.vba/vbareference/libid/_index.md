---
title: VbaReference.LibId
second_title: Aspose.Words for .NET API 参考
description: VbaReference 财产. 获取一个包含自动化类型库标识符的字符串值
type: docs
weight: 10
url: /zh/net/aspose.words.vba/vbareference/libid/
---
## VbaReference.LibId property

获取一个包含自动化类型库标识符的字符串值。

```csharp
public abstract string LibId { get; }
```

### 评论

根据引用类型，该属性的值可以是：

* 在 [MS-OVBA] 的 2.1.1.8 LibidReference 中指定的 LibidReference： https://docs.microsoft.com/en-us/openspecs/office_file_formats/ms-ovba/3737ef6e-d819-4186-a5f2-6e258ddf66a5
* 在 [MS-OVBA] 的 2.1.1.12 ProjectReference 指定的 ProjectReference： https://docs.microsoft.com/en-us/openspecs/office_file_formats/ms-ovba/9a45ac1a-f1ff-4ebd-958e-537701aa8131

### 例子

显示如何从 VBA 引用集合中获取/删除元素。

```csharp
[Test]
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

* class [VbaReference](../)
* 命名空间 [Aspose.Words.Vba](../../vbareference/)
* 部件 [Aspose.Words](../../../)


