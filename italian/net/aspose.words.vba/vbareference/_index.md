---
title: VbaReference Class
linktitle: VbaReference
articleTitle: VbaReference
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Vba.VbaReference per una perfetta integrazione con le librerie di tipi di automazione e i progetti VBA. Migliora l'automazione dei tuoi documenti oggi stesso!
type: docs
weight: 7440
url: /it/net/aspose.words.vba/vbareference/
---
## VbaReference class

Implementa un riferimento a una libreria di tipi di automazione o a un progetto VBA.

Per saperne di più, visita il[Lavorare con le macro VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) articolo di documentazione.

```csharp
public abstract class VbaReference
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| abstract [LibId](../../aspose.words.vba/vbareference/libid/) { get; } | Ottiene un valore stringa contenente l'identificatore di una libreria di tipi di automazione. |
| abstract [Type](../../aspose.words.vba/vbareference/type/) { get; } | Ottiene[`VbaReferenceType`](../vbareferencetype/) oggetto che indica il tipo di riferimento che un`VbaReference` l'oggetto rappresenta. |

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
