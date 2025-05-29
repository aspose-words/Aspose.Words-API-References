---
title: VbaReferenceType Enum
linktitle: VbaReferenceType
articleTitle: VbaReferenceType
second_title: Aspose.Words för .NET
description: Upptäck enumereringen Aspose.Words.Vba.VbaReferenceType för att enkelt definiera VbaReference-objekttyper, vilket förbättrar din dokumentautomation och -hantering.
type: docs
weight: 7460
url: /sv/net/aspose.words.vba/vbareferencetype/
---
## VbaReferenceType enumeration

Gör det möjligt att ange typen av en[`VbaReference`](../vbareference/) objekt.

```csharp
public enum VbaReferenceType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Registered | `13` | Anger en referenstyp för automationsbiblioteket. |
| Project | `14` | Angav en extern VBA-projektreferenstyp. |
| Original | `51` | Anger en ursprunglig referenstyp för automationsbiblioteket. |
| Control | `47` | Anger en referenstyp för ett twiddled-bibliotek. |

## Exempel

Visar hur man hämtar/tar bort ett element från VBA-referenssamlingen.

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
 /// Returnerar strängen som representerar LibId-sökvägen för en specificerad referens.
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
/// Returnerar sökvägen från en specificerad identifierare för ett bibliotek med automationstyper.
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
/// Returnerar sökvägen från en specificerad identifierare för ett bibliotek med automationstyper.
/// </summary>
private static string GetLibIdProjectPath(string libIdProject)
{
    return libIdProject != null ? libIdProject.Substring(3) : "";
}
```

### Se även

* namnutrymme [Aspose.Words.Vba](../../aspose.words.vba/)
* hopsättning [Aspose.Words](../../)
