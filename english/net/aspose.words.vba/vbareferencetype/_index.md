---
title: VbaReferenceType Enum
linktitle: VbaReferenceType
articleTitle: VbaReferenceType
second_title: Aspose.Words for .NET
description: Aspose.Words.Vba.VbaReferenceType enum. Allows to specify the type of a VbaReference object in C#.
type: docs
weight: 6650
url: /net/aspose.words.vba/vbareferencetype/
---
## VbaReferenceType enumeration

Allows to specify the type of a [`VbaReference`](../vbareference/) object.

```csharp
public enum VbaReferenceType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Registered | `13` | Specifies an Automation type library reference type. |
| Project | `14` | Specified an external VBA project reference type. |
| Original | `51` | Specifies an original Automation type library reference type. |
| Control | `47` | Specifies a twiddled type library reference type. |

## Examples

Shows how to get/remove an element from the VBA reference collection.

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
/// Returns string representing LibId path of a specified reference. 
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
/// Returns path from a specified identifier of an Automation type library.
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
/// Returns path from a specified identifier of an Automation type library.
/// </summary>
private static string GetLibIdProjectPath(string libIdProject)
{
    return libIdProject != null ? libIdProject.Substring(3) : "";
}
```

### See Also

* namespace [Aspose.Words.Vba](../../aspose.words.vba/)
* assembly [Aspose.Words](../../)
