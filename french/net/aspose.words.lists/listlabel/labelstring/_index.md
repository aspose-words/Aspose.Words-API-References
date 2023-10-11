---
title: ListLabel.LabelString
second_title: Référence de l'API Aspose.Words pour .NET
description: ListLabel propriété. Obtient une représentation sous forme de chaîne de létiquette de la liste.
type: docs
weight: 20
url: /fr/net/aspose.words.lists/listlabel/labelstring/
---
## ListLabel.LabelString property

Obtient une représentation sous forme de chaîne de l'étiquette de la liste.

```csharp
public string LabelString { get; }
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

* class [ListLabel](../)
* espace de noms [Aspose.Words.Lists](../../listlabel/)
* Assemblée [Aspose.Words](../../../)


