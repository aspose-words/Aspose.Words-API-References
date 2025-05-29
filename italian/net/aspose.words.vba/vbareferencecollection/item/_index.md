---
title: VbaReferenceCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi facilmente all'oggetto VbaReference con la proprietà Item. Recupera in modo efficiente i riferimenti tramite indice per uno sviluppo VBA semplificato.
type: docs
weight: 20
url: /it/net/aspose.words.vba/vbareferencecollection/item/
---
## VbaReferenceCollection indexer

Ottiene[`VbaReference`](../../vbareference/) oggetto all'indice specificato.

```csharp
public VbaReference this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Indice a partire da zero del riferimento da ottenere. |

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

* class [VbaReference](../../vbareference/)
* class [VbaReferenceCollection](../)
* spazio dei nomi [Aspose.Words.Vba](../../../aspose.words.vba/)
* assemblea [Aspose.Words](../../../)
