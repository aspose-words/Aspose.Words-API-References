---
title: Class ListLabel
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Lists.ListLabel classe. Définit les propriétés spécifiques à une étiquette de liste.
type: docs
weight: 3490
url: /fr/net/aspose.words.lists/listlabel/
---
## ListLabel class

Définit les propriétés spécifiques à une étiquette de liste.

Pour en savoir plus, visitez le[Travailler avec des listes](https://docs.aspose.com/words/net/working-with-lists/) article documentaire.

```csharp
public class ListLabel
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Font](../../aspose.words.lists/listlabel/font/) { get; } | Obtient la police de l'étiquette de la liste. |
| [LabelString](../../aspose.words.lists/listlabel/labelstring/) { get; } | Obtient une représentation sous forme de chaîne de l'étiquette de la liste. |
| [LabelValue](../../aspose.words.lists/listlabel/labelvalue/) { get; } | Obtient une valeur numérique pour cette étiquette. |

### Exemples

Montre comment extraire les étiquettes de liste de tous les paragraphes qui sont des éléments de liste.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Trouve si nous avons la liste des paragraphes. Dans notre document, notre liste utilise des chiffres arabes simples,
// qui commence à trois heures et se termine à six heures.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Il s'agit du texte que nous obtenons lorsque nous extrayons ce nœud au format texte.
     // Cette sortie texte omettra les étiquettes de liste. Coupez tous les caractères de formatage de paragraphe.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Ceci obtient la position du paragraphe dans le niveau actuel de la liste. Si nous avons une liste à plusieurs niveaux,
    // cela nous dira quelle est sa position à ce niveau.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Combinez-les ensemble pour inclure l'étiquette de liste avec le texte dans la sortie.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Voir également

* espace de noms [Aspose.Words.Lists](../../aspose.words.lists/)
* Assemblée [Aspose.Words](../../)


