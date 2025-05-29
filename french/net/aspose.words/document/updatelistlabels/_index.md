---
title: Document.UpdateListLabels
linktitle: UpdateListLabels
articleTitle: UpdateListLabels
second_title: Aspose.Words pour .NET
description: Mettez à jour sans effort toutes les étiquettes des éléments de liste de votre document avec la méthode UpdateListLabels, garantissant ainsi la cohérence et la clarté de votre contenu.
type: docs
weight: 820
url: /fr/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

Met à jour les étiquettes de liste pour tous les éléments de liste du document.

```csharp
public void UpdateListLabels()
```

## Remarques

Cette méthode met à jour les propriétés des étiquettes de liste telles que[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) et [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/) pour chaque[`ListLabel`](../../paragraph/listlabel/) objet dans le document.

De plus, cette méthode est parfois appelée implicitement lors de la mise à jour de champs du document. Cette méthode est required , car certains champs pouvant référencer des numéros de liste (comme TOC ou REF) doivent être à jour.

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

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
