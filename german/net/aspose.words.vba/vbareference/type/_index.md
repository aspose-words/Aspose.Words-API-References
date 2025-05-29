---
title: VbaReference.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: Entdecken Sie die VbaReference-Type-Eigenschaft, um VbaReferenceType-Objekte effektiv zu identifizieren und zu nutzen und so Ihre VBA-Programmiereffizienz zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.vba/vbareference/type/
---
## VbaReference.Type property

Ruft ab[`VbaReferenceType`](../../vbareferencetype/) Objekt, das den Typ der Referenz angibt, die ein[`VbaReference`](../) Objekt repräsentiert.

```csharp
public abstract VbaReferenceType Type { get; }
```

## Beispiele

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
    /// Gibt eine Zeichenfolge zurück, die den LibId-Pfad einer angegebenen Referenz darstellt.
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

* enum [VbaReferenceType](../../vbareferencetype/)
* class [VbaReference](../)
* namensraum [Aspose.Words.Vba](../../../aspose.words.vba/)
* Montage [Aspose.Words](../../../)
