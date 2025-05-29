---
title: Hyphenation.UnregisterDictionary
linktitle: UnregisterDictionary
articleTitle: UnregisterDictionary
second_title: Aspose.Words pour .NET
description: Supprimez sans effort les dictionnaires de césure pour n'importe quelle langue avec la méthode UnregisterDictionary, améliorant ainsi la clarté et la lisibilité du texte.
type: docs
weight: 50
url: /fr/net/aspose.words/hyphenation/unregisterdictionary/
---
## Hyphenation.UnregisterDictionary method

Annule l'enregistrement d'un dictionnaire de césure pour la langue spécifiée.

Ceci est différent de l'enregistrement d'un dictionnaire nul. Désenregistrer un dictionnaire active le rappel pour la langue spécifiée.

```csharp
public static void UnregisterDictionary(string language)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| language | String | Nom de langue, par exemple « en-US ». Consultez la documentation .NET pour « nom de culture » et la RFC 4646 pour plus de détails. |

## Exemples

Montre comment enregistrer un dictionnaire de césure.

```csharp
// Un dictionnaire de césure contient une liste de chaînes qui définissent les règles de césure pour la langue du dictionnaire.
// Lorsqu'un document contient des lignes de texte dans lesquelles un mot pourrait être divisé et continué sur la ligne suivante,
// la césure recherchera dans la liste des chaînes du dictionnaire les sous-chaînes de ce mot.
// Si le dictionnaire contient une sous-chaîne, la césure divisera le mot sur deux lignes
// par la sous-chaîne et ajoutez un trait d'union à la première moitié.
// Enregistrez un fichier de dictionnaire du système de fichiers local dans les paramètres régionaux « de-CH ».
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Ouvrir un document contenant du texte avec une locale correspondant à celle de notre dictionnaire,
// et enregistrez-le dans un format à pages fixes. Le texte de ce document sera coupé.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Recharger le document après avoir désenregistré le dictionnaire,
// et enregistrez-le dans un autre PDF, qui n'aura pas de texte coupé.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### Voir également

* class [Hyphenation](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
