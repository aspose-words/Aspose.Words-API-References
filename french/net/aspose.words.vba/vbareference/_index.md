---
title: VbaReference Class
linktitle: VbaReference
articleTitle: VbaReference
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Vba.VbaReference pour une intégration fluide avec les bibliothèques de types Automation et les projets VBA. Optimisez l'automatisation de vos documents dès aujourd'hui !
type: docs
weight: 7440
url: /fr/net/aspose.words.vba/vbareference/
---
## VbaReference class

Implémente une référence à une bibliothèque de types Automation ou à un projet VBA.

Pour en savoir plus, visitez le[Travailler avec les macros VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) article de documentation.

```csharp
public abstract class VbaReference
```

## Propriétés

| Nom | La description |
| --- | --- |
| abstract [LibId](../../aspose.words.vba/vbareference/libid/) { get; } | Obtient une valeur de chaîne contenant l'identifiant d'une bibliothèque de types Automation. |
| abstract [Type](../../aspose.words.vba/vbareference/type/) { get; } | Obtient[`VbaReferenceType`](../vbareferencetype/) objet qui indique le type de référence qu'un`VbaReference` l'objet représente. |

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
