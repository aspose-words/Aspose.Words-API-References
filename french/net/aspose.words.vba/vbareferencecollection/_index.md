---
title: VbaReferenceCollection Class
linktitle: VbaReferenceCollection
articleTitle: VbaReferenceCollection
second_title: Aspose.Words pour .NET
description: Explorez la classe Aspose.Words.Vba.VbaReferenceCollection, un outil puissant pour gérer efficacement les objets VbaReference dans vos projets.
type: docs
weight: 7450
url: /fr/net/aspose.words.vba/vbareferencecollection/
---
## VbaReferenceCollection class

Représente une collection de[`VbaReference`](../vbareference/) objets.

Pour en savoir plus, visitez le[Travailler avec les macros VBA](https://docs.aspose.com/words/net/working-with-vba-macros/) article de documentation.

```csharp
public sealed class VbaReferenceCollection : IEnumerable<VbaReference>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.vba/vbareferencecollection/count/) { get; } | Renvoie le nombre de références VBA dans la collection. |
| [Item](../../aspose.words.vba/vbareferencecollection/item/) { get; } | Obtient[`VbaReference`](../vbareference/) objet à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Remove](../../aspose.words.vba/vbareferencecollection/remove/)(*[VbaReference](../vbareference/)*) | Supprime la première occurrence d'un élément spécifié[`VbaReference`](../vbareference/) article de la collection. |
| [RemoveAt](../../aspose.words.vba/vbareferencecollection/removeat/)(*int*) | Supprime le[`VbaReference`](../vbareference/) élément à l'index spécifié de la collection. |

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

* class [VbaReference](../vbareference/)
* espace de noms [Aspose.Words.Vba](../../aspose.words.vba/)
* Assemblée [Aspose.Words](../../)
