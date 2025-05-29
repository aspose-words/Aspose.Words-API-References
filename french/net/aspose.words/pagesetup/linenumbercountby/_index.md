---
title: PageSetup.LineNumberCountBy
linktitle: LineNumberCountBy
articleTitle: LineNumberCountBy
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PageSetup LineNumberCountBy pour personnaliser facilement les incréments de numéros de ligne pour une mise en forme et une lisibilité améliorées du document.
type: docs
weight: 210
url: /fr/net/aspose.words/pagesetup/linenumbercountby/
---
## PageSetup.LineNumberCountBy property

Renvoie ou définit l'incrément numérique pour les numéros de ligne.

```csharp
public int LineNumberCountBy { get; set; }
```

## Exemples

Montre comment activer la numérotation des lignes pour une section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nous pouvons utiliser l'objet PageSetup de la section pour afficher les numéros à gauche des lignes de texte de la section.
// C'est le même comportement qu'un objet List,
// mais il couvre toute la section et ne modifie en aucune façon le texte.
// Notre section recommencera la numérotation sur chaque nouvelle page à partir de 1 et affichera le numéro,
// s'il s'agit d'un multiple de 3, à 50pt à gauche de la ligne.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// Le compteur de lignes ignorera tout paragraphe avec l'indicateur « SuppressLineNumbers » défini sur « true ».
// Ce paragraphe est sur la 15e ligne, qui est un multiple de 3, et afficherait donc normalement un numéro de ligne.
// Le compteur de lignes de la section ignorera également cette ligne, traitera la ligne suivante comme la 15e,
// et continuez le décompte à partir de ce point.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
