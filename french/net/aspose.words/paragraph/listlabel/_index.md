---
title: Paragraph.ListLabel
second_title: Référence de l'API Aspose.Words pour .NET
description: Paragraph propriété. Obtient unListLabelobjet qui donne accès à la valeur de numérotation de la liste et au formatting pour ce paragraphe.
type: docs
weight: 160
url: /fr/net/aspose.words/paragraph/listlabel/
---
## Paragraph.ListLabel property

Obtient un`ListLabel`objet qui donne accès à la valeur de numérotation de la liste et au formatting pour ce paragraphe.

```csharp
public ListLabel ListLabel { get; }
```

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

* class [ListLabel](../../../aspose.words.lists/listlabel/)
* class [Paragraph](../)
* espace de noms [Aspose.Words](../../paragraph/)
* Assemblée [Aspose.Words](../../../)


