---
title: Document.UpdateListLabels
second_title: Référence de l'API Aspose.Words pour .NET
description: Document méthode. Met à jour les étiquettes de liste pour tous les éléments de liste du document.
type: docs
weight: 780
url: /fr/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

Met à jour les étiquettes de liste pour tous les éléments de liste du document.

```csharp
public void UpdateListLabels()
```

### Remarques

Cette méthode met à jour les propriétés des étiquettes de liste telles que[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) et [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/) pour chaque[`ListLabel`](../../paragraph/listlabel/)objet dans le document.

De plus, cette méthode est parfois appelée implicitement lors de la mise à jour des champs du document. Ceci est requis car certains champs pouvant faire référence à des numéros de liste (tels que TOC ou REF) ont besoin qu'ils soient à jour.

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

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


