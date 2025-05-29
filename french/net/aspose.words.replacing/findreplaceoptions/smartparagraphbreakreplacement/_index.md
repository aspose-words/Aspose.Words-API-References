---
title: FindReplaceOptions.SmartParagraphBreakReplacement
linktitle: SmartParagraphBreakReplacement
articleTitle: SmartParagraphBreakReplacement
second_title: Aspose.Words pour .NET
description: Découvrez la propriété SmartParagraphBreakReplacement dans FindReplaceOptions. Contrôlez facilement les sauts de paragraphe pour une mise en forme fluide du texte.
type: docs
weight: 170
url: /fr/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

Obtient ou définit une valeur booléenne indiquant qu'il est autorisé de remplacer le paragraphe break lorsqu'il n'y a pas de paragraphe frère suivant.

La valeur par défaut est`FAUX`.

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

## Remarques

Cette option permet de remplacer le saut de paragraphe lorsqu'il n'y a pas de paragraphe frère suivant vers lequel tous les nœuds enfants peuvent être déplacés, en trouvant n'importe quel paragraphe suivant (pas nécessairement frère) après le paragraphe remplacé.

## Exemples

Montre comment supprimer un paragraphe d'une cellule de tableau avec un tableau imbriqué.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Créer un tableau avec un paragraphe et un tableau intérieur dans la première cellule.
builder.StartTable();
builder.InsertCell();
builder.Write("TEXT1");
builder.StartTable();
builder.InsertCell();
builder.EndTable();
builder.EndTable();
builder.Writeln();

FindReplaceOptions options = new FindReplaceOptions();
// Lorsque l'option suivante est définie sur « true », Aspose.Words supprimera le texte du paragraphe
// avec sa marque de paragraphe. Sinon, Aspose.Words imitera Word et supprimera
// uniquement le texte du paragraphe et laisse la marque de paragraphe intacte (lorsqu'un tableau suit le texte).
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### Voir également

* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../../)
