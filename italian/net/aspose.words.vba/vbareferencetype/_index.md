---
title: VbaReferenceType Enum
linktitle: VbaReferenceType
articleTitle: VbaReferenceType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Vba.VbaReferenceType per definire facilmente i tipi di oggetti VbaReference, migliorando così l'automazione e la gestione dei documenti.
type: docs
weight: 7460
url: /it/net/aspose.words.vba/vbareferencetype/
---
## VbaReferenceType enumeration

Consente di specificare il tipo di a[`VbaReference`](../vbareference/) oggetto.

```csharp
public enum VbaReferenceType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Registered | `13` | Specifica un tipo di riferimento alla libreria di tipo Automation. |
| Project | `14` | Specificato un tipo di riferimento al progetto VBA esterno. |
| Original | `51` | Specifica un tipo di riferimento alla libreria di tipo Automation originale. |
| Control | `47` | Specifica un tipo di riferimento alla libreria di tipi modificati. |

## Esempi

Mostra come ottenere/rimuovere un elemento dalla raccolta di riferimenti VBA.

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
 /// Restituisce una stringa che rappresenta il percorso LibId di un riferimento specificato.
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
/// Restituisce il percorso da un identificatore specificato di una libreria di tipi di automazione.
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
/// Restituisce il percorso da un identificatore specificato di una libreria di tipi di automazione.
/// </summary>
private static string GetLibIdProjectPath(string libIdProject)
{
    return libIdProject != null ? libIdProject.Substring(3) : "";
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Vba](../../aspose.words.vba/)
* assemblea [Aspose.Words](../../)
