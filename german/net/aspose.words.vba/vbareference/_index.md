---
title: Class VbaReference
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Vba.VbaReference klas. Implementiert einen Verweis auf eine Automatisierungstypbibliothek oder ein VBAProjekt.
type: docs
weight: 6590
url: /de/net/aspose.words.vba/vbareference/
---
## VbaReference class

Implementiert einen Verweis auf eine Automatisierungstypbibliothek oder ein VBA-Projekt.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit VBA-Makros](https://docs.aspose.com/words/net/working-with-vba-macros/) Dokumentationsartikel.

```csharp
public abstract class VbaReference
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| abstract [LibId](../../aspose.words.vba/vbareference/libid/) { get; } | Ruft einen Zeichenfolgenwert ab, der den Bezeichner einer Automatisierungstypbibliothek enthält. |
| abstract [Type](../../aspose.words.vba/vbareference/type/) { get; } | Ruft ab[`VbaReferenceType`](../vbareferencetype/) Objekt, das die Art der Referenz angibt, die a`VbaReference` Objekt repräsentiert. |

### Beispiele

Zeigt, wie ein Element aus der VBA-Referenzsammlung abgerufen/entfernt wird.

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
 /// Gibt einen String zurück, der den LibId-Pfad einer angegebenen Referenz darstellt.
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
/// Gibt den Pfad von einem angegebenen Bezeichner einer Automatisierungstypbibliothek zurück.
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
/// Gibt den Pfad von einem angegebenen Bezeichner einer Automatisierungstypbibliothek zurück.
/// </summary>
private static string GetLibIdProjectPath(string libIdProject)
{
    return libIdProject != null ? libIdProject.Substring(3) : "";
}
```

### Siehe auch

* namensraum [Aspose.Words.Vba](../../aspose.words.vba/)
* Montage [Aspose.Words](../../)


