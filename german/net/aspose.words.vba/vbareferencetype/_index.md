---
title: VbaReferenceType Enum
linktitle: VbaReferenceType
articleTitle: VbaReferenceType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Vba.VbaReferenceType, um VbaReference-Objekttypen einfach zu definieren und so Ihre Dokumentenautomatisierung und -verwaltung zu verbessern.
type: docs
weight: 7460
url: /de/net/aspose.words.vba/vbareferencetype/
---
## VbaReferenceType enumeration

Ermöglicht die Angabe des Typs eines[`VbaReference`](../vbareference/) Objekt.

```csharp
public enum VbaReferenceType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Registered | `13` | Gibt einen Referenztyp für die Automatisierungstypbibliothek an. |
| Project | `14` | Es wurde ein externer VBA-Projektverweistyp angegeben. |
| Original | `51` | Gibt einen ursprünglichen Referenztyp der Automatisierungstypbibliothek an. |
| Control | `47` | Gibt einen Referenztyp für eine Twiddled-Typbibliothek an. |

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

* namensraum [Aspose.Words.Vba](../../aspose.words.vba/)
* Montage [Aspose.Words](../../)
