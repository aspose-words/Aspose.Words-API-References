---
title: Paragraph.ListLabel
second_title: Référence de l'API Aspose.Words pour .NET
description: Paragraph propriété. Obtient unListLabel objet qui donne accès à la valeur de numérotation de la liste et au formatage pour ce paragraphe.
type: docs
weight: 160
url: /fr/net/aspose.words/paragraph/listlabel/
---
## Paragraph.ListLabel property

Obtient un`ListLabel` objet qui donne accès à la valeur de numérotation de la liste et au formatage pour ce paragraphe.

```csharp
public ListLabel ListLabel { get; }
```

### Exemples

Montre comment extraire les étiquettes de liste de tous les paragraphes qui sont des éléments de liste.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Recherche si nous avons la liste des paragraphes. Dans notre document, notre liste utilise des chiffres arabes simples,
// qui commence à trois et se termine à six.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // C'est le texte que nous obtenons lorsque nous obtenons ce nœud au format texte.
    // Cette sortie de texte omettra les étiquettes de liste. Coupez tous les caractères de formatage de paragraphe. 
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Cela obtient la position du paragraphe dans le niveau actuel de la liste. Si nous avons une liste à plusieurs niveaux,
    // cela nous dira quelle position il est à ce niveau.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Combinez-les pour inclure l'étiquette de la liste avec le texte dans la sortie.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Voir également

* class [ListLabel](../../../aspose.words.lists/listlabel/)
* class [Paragraph](../)
* espace de noms [Aspose.Words](../../paragraph/)
* Assemblée [Aspose.Words](../../../)


