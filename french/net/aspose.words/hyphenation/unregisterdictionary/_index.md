---
title: Hyphenation.UnregisterDictionary
linktitle: UnregisterDictionary
articleTitle: UnregisterDictionary
second_title: Aspose.Words pour .NET
description: Hyphenation UnregisterDictionary méthode. Désenregistre un dictionnaire de césure pour la langue spécifiée en C#.
type: docs
weight: 50
url: /fr/net/aspose.words/hyphenation/unregisterdictionary/
---
## Hyphenation.UnregisterDictionary method

Désenregistre un dictionnaire de césure pour la langue spécifiée.

Ceci est différent de l'enregistrement du dictionnaire Null. La désinscription d'un dictionnaire active le rappel pour la langue spécifiée.

```csharp
public static void UnregisterDictionary(string language)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| language | String | Un nom de langue, par exemple "en-US". Consultez la documentation .NET pour le « nom de la culture » et la RFC 4646 pour plus de détails. |

## Exemples

Montre comment enregistrer un dictionnaire de césure.

```csharp
// Un dictionnaire de césure contient une liste de chaînes qui définissent les règles de césure pour la langue du dictionnaire.
// Lorsqu'un document contient des lignes de texte dans lesquelles un mot pourrait être découpé et continué sur la ligne suivante,
// La césure recherchera dans la liste des chaînes du dictionnaire les sous-chaînes de ce mot.
// Si le dictionnaire contient une sous-chaîne, alors la césure divisera le mot sur deux lignes
// par la sous-chaîne et ajoutez un trait d'union à la première moitié.
// Enregistrez un fichier de dictionnaire du système de fichiers local dans la locale "de-CH".
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Ouvre un document contenant du texte avec une locale correspondant à celle de notre dictionnaire,
// et enregistrez-le dans un format de sauvegarde de page fixe. Le texte de ce document sera coupé.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Recharge le document après avoir désenregistré le dictionnaire,
// et enregistrez-le dans un autre PDF, qui ne contiendra pas de texte avec trait d'union.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### Voir également

* class [Hyphenation](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
