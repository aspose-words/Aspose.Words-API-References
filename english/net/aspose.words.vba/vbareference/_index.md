---
title: VbaReference Class
linktitle: VbaReference
articleTitle: VbaReference
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Vba.VbaReference class for seamless integration with Automation type libraries and VBA projects. Enhance your document automation today!
type: docs
weight: 7440
url: /net/aspose.words.vba/vbareference/
---
## VbaReference class

Implements a reference to an Automation type library or VBA project.

To learn more, visit the [Working with VBA Macros](https://docs.aspose.com/words/net/working-with-vba-macros/) documentation article.

```csharp
public abstract class VbaReference
```

## Properties

| Name | Description |
| --- | --- |
| abstract [LibId](../../aspose.words.vba/vbareference/libid/) { get; } | Gets a string value containing the identifier of an Automation type library. |
| abstract [Type](../../aspose.words.vba/vbareference/type/) { get; } | Gets [`VbaReferenceType`](../vbareferencetype/) object that indicates the type of reference that a `VbaReference` object represents. |

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
