---
title: VbaReferenceCollection Class
linktitle: VbaReferenceCollection
articleTitle: VbaReferenceCollection
second_title: Aspose.Words för .NET
description: Utforska klassen Aspose.Words.Vba.VbaReferenceCollection, ett kraftfullt verktyg för att effektivt hantera VbaReference-objekt i dina projekt.
type: docs
weight: 7450
url: /sv/net/aspose.words.vba/vbareferencecollection/
---
## VbaReferenceCollection class

Representerar en samling av[`VbaReference`](../vbareference/) objekt.

För att lära dig mer, besök[Arbeta med VBA-makron](https://docs.aspose.com/words/net/working-with-vba-macros/) dokumentationsartikel.

```csharp
public sealed class VbaReferenceCollection : IEnumerable<VbaReference>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.vba/vbareferencecollection/count/) { get; } | Returnerar antalet VBA-referenser i samlingen. |
| [Item](../../aspose.words.vba/vbareferencecollection/item/) { get; } | Får[`VbaReference`](../vbareference/) objekt vid det angivna indexet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Remove](../../aspose.words.vba/vbareferencecollection/remove/)(*[VbaReference](../vbareference/)*) | Tar bort den första förekomsten av en specifik[`VbaReference`](../vbareference/) föremål från samlingen. |
| [RemoveAt](../../aspose.words.vba/vbareferencecollection/removeat/)(*int*) | Tar bort[`VbaReference`](../vbareference/) element vid det angivna indexet för samlingen. |

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

* class [VbaReference](../vbareference/)
* namnutrymme [Aspose.Words.Vba](../../aspose.words.vba/)
* hopsättning [Aspose.Words](../../)
