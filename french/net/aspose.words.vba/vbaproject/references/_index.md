---
title: VbaProject.References
linktitle: References
articleTitle: References
second_title: Aspose.Words pour .NET
description: Explorez la propriété Références de projet VBA pour gérer efficacement vos références de projet VBA et améliorer vos compétences de codage. Libérez votre potentiel de programmation !
type: docs
weight: 70
url: /fr/net/aspose.words.vba/vbaproject/references/
---
## VbaProject.References property

Obtient une collection de références de projets VBA.

```csharp
public VbaReferenceCollection References { get; }
```

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

* class [VbaReferenceCollection](../../vbareferencecollection/)
* class [VbaProject](../)
* espace de noms [Aspose.Words.Vba](../../../aspose.words.vba/)
* Assemblée [Aspose.Words](../../../)
