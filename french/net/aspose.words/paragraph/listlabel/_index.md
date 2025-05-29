---
title: Paragraph.ListLabel
linktitle: ListLabel
articleTitle: ListLabel
second_title: Aspose.Words pour .NET
description: Accédez à la numérotation des listes et formatez-la avec la propriété Paragraph ListLabel. Améliorez l'organisation et la clarté de votre document sans effort !
type: docs
weight: 160
url: /fr/net/aspose.words/paragraph/listlabel/
---
## Paragraph.ListLabel property

Obtient un`ListLabel`objet qui donne accès à la valeur de numérotation de liste et au formatage pour ce paragraphe.

```csharp
public ListLabel ListLabel { get; }
```

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

* class [ListLabel](../../../aspose.words.lists/listlabel/)
* class [Paragraph](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
