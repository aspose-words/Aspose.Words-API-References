---
title: Enum LineNumberRestartMode
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.LineNumberRestartMode énumération. Détermine quand la numérotation automatique des lignes redémarre.
type: docs
weight: 3430
url: /fr/net/aspose.words/linenumberrestartmode/
---
## LineNumberRestartMode enumeration

Détermine quand la numérotation automatique des lignes redémarre.

```csharp
public enum LineNumberRestartMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| RestartPage | `0` | La numérotation des lignes redémarre au début de chaque page. |
| RestartSection | `1` | La numérotation des lignes recommence au début de la section. |
| Continuous | `2` | Numérotation des lignes continue de la section précédente. |

### Exemples

Montre comment activer la numérotation des lignes pour une section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nous pouvons utiliser l'objet PageSetup de la section pour afficher les nombres à gauche des lignes de texte de la section.
// C'est le même comportement qu'un objet List,
// mais il couvre toute la section et ne modifie en rien le texte.
// Notre rubrique va relancer la numérotation à chaque nouvelle page à partir de 1 et afficher le numéro,
// si c'est un multiple de 3, à 50pt à gauche de la ligne.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// Le compteur de lignes ignorera tout paragraphe dont l'indicateur "SuppressLineNumbers" est défini sur "true".
// Ce paragraphe se trouve sur la 15ème ligne, qui est un multiple de 3, et afficherait donc normalement un numéro de ligne.
// Le compteur de lignes de la section ignorera également cette ligne, traitera la ligne suivante comme la 15ème,
// et continuez le décompte à partir de ce moment.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### Voir également

* class [PageSetup](../pagesetup/)
* property [LineNumberRestartMode](../pagesetup/linenumberrestartmode/)
* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)


