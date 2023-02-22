---
title: Node.ToString
second_title: Référence de l'API Aspose.Words pour .NET
description: Node méthode. Exporte le contenu du nœud dans une chaîne au format spécifié.
type: docs
weight: 160
url: /fr/net/aspose.words/node/tostring/
---
## ToString(SaveFormat) {#tostring_1}

Exporte le contenu du nœud dans une chaîne au format spécifié.

```csharp
public string ToString(SaveFormat saveFormat)
```

### Return_Value

Le contenu du nœud dans le format spécifié.

### Exemples

Montre la différence entre l'appel des méthodes GetText et ToString sur un nœud.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText va récupérer le texte visible ainsi que les codes de champs et les caractères spéciaux.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString nous donnera l'apparence du document s'il est enregistré dans un format d'enregistrement passé.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

Exporte le contenu d'un nœud vers String au format HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Lorsque nous appelons la méthode ToString à l'aide de la surcharge html SaveFormat,
// il convertit le contenu du nœud en sa représentation html brute.
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

* enum [SaveFormat](../../saveformat/)
* class [Node](../)
* espace de noms [Aspose.Words](../../node/)
* Assemblée [Aspose.Words](../../../)

---

## ToString(SaveOptions) {#tostring_2}

Exporte le contenu du nœud dans une chaîne à l'aide des options d'enregistrement spécifiées.

```csharp
public string ToString(SaveOptions saveOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| saveOptions | SaveOptions | Spécifie les options qui contrôlent la façon dont le nœud est enregistré. |

### Return_Value

Le contenu du nœud dans le format spécifié.

### Exemples

Exporte le contenu d'un nœud vers String au format HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Lorsque nous appelons la méthode ToString à l'aide de la surcharge html SaveFormat,
// il convertit le contenu du nœud en sa représentation html brute.
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
* espace de noms [Aspose.Words](../../node/)
* Assemblée [Aspose.Words](../../../)


