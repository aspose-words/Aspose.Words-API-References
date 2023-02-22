---
title: Class VbaReferenceCollection
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Vba.VbaReferenceCollection classe. Rappresenta una raccolta diVbaReference oggetti.
type: docs
weight: 6290
url: /it/net/aspose.words.vba/vbareferencecollection/
---
## VbaReferenceCollection class

Rappresenta una raccolta di[`VbaReference`](../vbareference/) oggetti.

```csharp
public sealed class VbaReferenceCollection : IEnumerable<VbaReference>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.vba/vbareferencecollection/count/) { get; } | Restituisce il numero di riferimenti VBA nella raccolta. |
| [Item](../../aspose.words.vba/vbareferencecollection/item/) { get; } | Ottiene[`VbaReference`](../vbareference/) oggetto all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Remove](../../aspose.words.vba/vbareferencecollection/remove/)(VbaReference) | Rimuove la prima occorrenza di un elemento VbaReference specificato dalla raccolta. |
| [RemoveAt](../../aspose.words.vba/vbareferencecollection/removeat/)(int) | Rimuove l'elemento VbaReference in corrispondenza dell'indice specificato della raccolta. |

### Esempi

Mostra come ottenere/rimuovere un elemento dalla raccolta di riferimenti VBA.

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
/// Restituisce il percorso da un identificatore specificato di una libreria dei tipi di automazione.
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
/// Restituisce il percorso da un identificatore specificato di una libreria dei tipi di automazione.
/// </summary>
private static string GetLibIdProjectPath(string libIdProject)
{
    return libIdProject != null ? libIdProject.Substring(3) : "";
}
```

### Guarda anche

* class [VbaReference](../vbareference/)
* spazio dei nomi [Aspose.Words.Vba](../../aspose.words.vba/)
* assemblea [Aspose.Words](../../)


