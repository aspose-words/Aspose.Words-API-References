---
title: Class VbaReferenceCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Vba.VbaReferenceCollection klas. Repräsentiert eine Sammlung vonVbaReference Objekte.
type: docs
weight: 6290
url: /de/net/aspose.words.vba/vbareferencecollection/
---
## VbaReferenceCollection class

Repräsentiert eine Sammlung von[`VbaReference`](../vbareference/) Objekte.

```csharp
public sealed class VbaReferenceCollection : IEnumerable<VbaReference>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.vba/vbareferencecollection/count/) { get; } | Gibt die Anzahl der VBA-Referenzen in der Sammlung zurück. |
| [Item](../../aspose.words.vba/vbareferencecollection/item/) { get; } | erhält[`VbaReference`](../vbareference/) Objekt am angegebenen Index. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Remove](../../aspose.words.vba/vbareferencecollection/remove/)(VbaReference) | Entfernt das erste Vorkommen eines angegebenen VbaReference-Elements aus der Sammlung. |
| [RemoveAt](../../aspose.words.vba/vbareferencecollection/removeat/)(int) | Entfernt das VbaReference-Element am angegebenen Index der Sammlung. |

### Beispiele

Zeigt, wie ein Element aus der VBA-Referenzsammlung abgerufen/entfernt wird.

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

* class [VbaReference](../vbareference/)
* namensraum [Aspose.Words.Vba](../../aspose.words.vba/)
* Montage [Aspose.Words](../../)


