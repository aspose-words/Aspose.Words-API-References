---
title: ParagraphFormat.SuppressAutoHyphens
linktitle: SuppressAutoHyphens
articleTitle: SuppressAutoHyphens
second_title: Aspose.Words pour .NET
description: ParagraphFormat SuppressAutoHyphens propriété. Spécifie si le paragraphe actuel doit être exempté de toute césure qui est appliquée dans les paramètres du document en C#.
type: docs
weight: 370
url: /fr/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

Spécifie si le paragraphe actuel doit être exempté de toute césure qui est appliquée dans les paramètres du document.

```csharp
public bool SuppressAutoHyphens { get; set; }
```

## Exemples

Montre comment supprimer la césure d’un paragraphe.

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Ouvre un document contenant du texte avec une locale correspondant à celle de notre dictionnaire.
// Lorsque nous enregistrons ce document dans un format de sauvegarde de page fixe, son texte aura une césure.
Document doc = new Document(MyDir + "German text.docx");

// Nous pouvons définir la propriété "SuppressAutoHyphens" sur "true" pour désactiver la césure
// pour un paragraphe spécifique tout en le gardant activé pour le reste du document.
// La valeur par défaut de cette propriété est "false",
// ce qui signifie que chaque paragraphe utilise par défaut la césure si elle est disponible.
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### Voir également

* class [ParagraphFormat](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
