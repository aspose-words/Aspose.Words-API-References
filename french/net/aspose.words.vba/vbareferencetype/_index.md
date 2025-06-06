---
title: VbaReferenceType Enum
linktitle: VbaReferenceType
articleTitle: VbaReferenceType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Vba.VbaReferenceType pour définir facilement les types d'objets VbaReference, améliorant ainsi l'automatisation et la gestion de vos documents.
type: docs
weight: 7460
url: /fr/net/aspose.words.vba/vbareferencetype/
---
## VbaReferenceType enumeration

Permet de spécifier le type d'un[`VbaReference`](../vbareference/) objet.

```csharp
public enum VbaReferenceType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Registered | `13` | Spécifie un type de référence de bibliothèque de type Automation. |
| Project | `14` | Spécifie un type de référence de projet VBA externe. |
| Original | `51` | Spécifie un type de référence de bibliothèque de types d'automatisation d'origine. |
| Control | `47` | Spécifie un type de référence de bibliothèque de types modifié. |

## Exemples

Montre comment obtenir/supprimer un élément de la collection de référence VBA.

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
 /// Renvoie une chaîne représentant le chemin LibId d'une référence spécifiée.
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
/// Renvoie le chemin à partir d'un identifiant spécifié d'une bibliothèque de type Automation.
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
/// Renvoie le chemin à partir d'un identifiant spécifié d'une bibliothèque de type Automation.
/// </summary>
private static string GetLibIdProjectPath(string libIdProject)
{
    return libIdProject != null ? libIdProject.Substring(3) : "";
}
```

### Voir également

* espace de noms [Aspose.Words.Vba](../../aspose.words.vba/)
* Assemblée [Aspose.Words](../../)
