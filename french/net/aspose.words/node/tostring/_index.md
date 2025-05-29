---
title: Node.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words pour .NET
description: Découvrez la méthode Node ToString : convertissez facilement le contenu d'un nœud en chaînes de caractères aux formats personnalisables pour une gestion optimisée des données. Optimisez votre codage dès aujourd'hui !
type: docs
weight: 160
url: /fr/net/aspose.words/node/tostring/
---
## ToString(*[SaveFormat](../../saveformat/)*) {#tostring_1}

Exporte le contenu du nœud dans une chaîne au format spécifié.

```csharp
public string ToString(SaveFormat saveFormat)
```

### Return_Value

Le contenu du nœud dans le format spécifié.

## Exemples

Affiche la différence entre l’appel des méthodes GetText et ToString sur un nœud.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText récupérera le texte visible ainsi que les codes de champ et les caractères spéciaux.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015", doc.GetText().Trim());

// ToString nous donnera l'apparence du document s'il est enregistré dans un format d'enregistrement passé.
Assert.AreEqual("«Field»", doc.ToString(SaveFormat.Text).Trim());
```

Exporte le contenu d'un nœud vers une chaîne au format HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Lorsque nous appelons la méthode ToString en utilisant la surcharge HTML SaveFormat,
// il convertit le contenu du nœud en sa représentation HTML brute.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Nous pouvons également modifier le résultat de cette conversion à l'aide d'un objet SaveOptions.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

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

* enum [SaveFormat](../../saveformat/)
* class [Node](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## ToString(*[SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#tostring_2}

Exporte le contenu du nœud dans une chaîne en utilisant les options de sauvegarde spécifiées.

```csharp
public string ToString(SaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| saveOptions | SaveOptions | Spécifie les options qui contrôlent la manière dont le nœud est enregistré. |

### Return_Value

Le contenu du nœud dans le format spécifié.

## Exemples

Exporte le contenu d'un nœud vers une chaîne au format HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Lorsque nous appelons la méthode ToString en utilisant la surcharge HTML SaveFormat,
// il convertit le contenu du nœud en sa représentation HTML brute.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// Nous pouvons également modifier le résultat de cette conversion à l'aide d'un objet SaveOptions.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

### Voir également

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Node](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
