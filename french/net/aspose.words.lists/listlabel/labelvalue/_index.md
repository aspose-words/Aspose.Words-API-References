---
title: ListLabel.LabelValue
linktitle: LabelValue
articleTitle: LabelValue
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ListLabel LabelValue pour récupérer facilement les valeurs numériques des étiquettes, améliorant ainsi votre gestion des données et l'efficacité de vos rapports.
type: docs
weight: 30
url: /fr/net/aspose.words.lists/listlabel/labelvalue/
---
## ListLabel.LabelValue property

Obtient une valeur numérique pour cette étiquette.

```csharp
public int LabelValue { get; }
```

## Remarques

Utilisez le[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) méthode pour mettre à jour la valeur de cette propriété.

## Exemples

Montre comment extraire les étiquettes de liste de tous les paragraphes qui sont des éléments de liste.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Vérifiez si nous avons la liste des paragraphes. Dans notre document, notre liste utilise des chiffres arabes simples.
// qui commencent à trois heures et se terminent à six heures.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Il s'agit du texte que nous obtenons lorsque nous exportons ce nœud au format texte.
     // Ce texte affiché omettra les étiquettes de liste. Supprimez tous les caractères de formatage de paragraphe.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Ceci récupère la position du paragraphe dans le niveau actuel de la liste. Si la liste comporte plusieurs niveaux,
    // cela nous indiquera quelle position il occupe à ce niveau.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Combinez-les ensemble pour inclure l'étiquette de liste avec le texte dans la sortie.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Voir également

* class [ListLabel](../)
* espace de noms [Aspose.Words.Lists](../../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../../)
