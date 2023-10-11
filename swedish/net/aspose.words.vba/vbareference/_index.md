---
title: Class VbaReference
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Vba.VbaReference klass. Implementerar en referens till ett bibliotek av automationstyp eller VBAprojekt.
type: docs
weight: 6590
url: /sv/net/aspose.words.vba/vbareference/
---
## VbaReference class

Implementerar en referens till ett bibliotek av automationstyp eller VBA-projekt.

För att lära dig mer, besök[Arbeta med VBA-makron](https://docs.aspose.com/words/net/working-with-vba-macros/) dokumentationsartikel.

```csharp
public abstract class VbaReference
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| abstract [LibId](../../aspose.words.vba/vbareference/libid/) { get; } | Hämtar ett strängvärde som innehåller identifieraren för ett bibliotek av automationstyp. |
| abstract [Type](../../aspose.words.vba/vbareference/type/) { get; } | Blir[`VbaReferenceType`](../vbareferencetype/) objekt som anger vilken typ av referens som a`VbaReference` objekt representerar. |

### Exempel

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
 /// Returnerar en sträng som representerar LibId-sökvägen för en angiven referens.
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
/// Returnerar sökväg från en specificerad identifierare för ett bibliotek av automationstyp.
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
/// Returnerar sökväg från en specificerad identifierare för ett bibliotek av automationstyp.
/// </summary>
private static string GetLibIdProjectPath(string libIdProject)
{
    return libIdProject != null ? libIdProject.Substring(3) : "";
}
```

### Se även

* namnutrymme [Aspose.Words.Vba](../../aspose.words.vba/)
* hopsättning [Aspose.Words](../../)


