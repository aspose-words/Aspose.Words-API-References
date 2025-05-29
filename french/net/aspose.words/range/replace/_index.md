---
title: Range.Replace
linktitle: Replace
articleTitle: Replace
second_title: Aspose.Words pour .NET
description: Remplacez facilement toutes les occurrences d'un modèle de chaîne de caractères grâce à la méthode Range Replace. Améliorez votre traitement de texte grâce à cet outil puissant !
type: docs
weight: 100
url: /fr/net/aspose.words/range/replace/
---
## Replace(*string, string*) {#replace}

Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement.

```csharp
public int Replace(string pattern, string replacement)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| pattern | String | Une chaîne à remplacer. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |

### Return_Value

Le nombre de remplacements effectués.

## Remarques

Le modèle ne sera pas utilisé comme expression régulière. Veuillez utiliser`Replace` si vous avez besoin d'expressions régulières.

Comparaison insensible à la casse utilisée.

La méthode est capable de traiter les ruptures dans les chaînes de modèle et de remplacement.

Vous devez utiliser des méta-caractères spéciaux si vous devez travailler avec des sauts :

* **&amp;p** - saut de paragraphe
* **&amp;b** - saut de section
* **&amp;m** - saut de page
* **&amp;l** - saut de ligne manuel

Utiliser la méthode`Replace` pour avoir une personnalisation plus flexible.

## Exemples

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Insère un saut de paragraphe après Numbers.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Montre comment effectuer une opération de recherche et de remplacement de texte sur le contenu d'un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Greetings, _FullName_!");

// Effectuez une opération de recherche et de remplacement sur le contenu de notre document et vérifiez le nombre de remplacements qui ont eu lieu.
int replacementCount = doc.Range.Replace("_FullName_", "John Doe");

Assert.AreEqual(1, replacementCount);
Assert.AreEqual("Greetings, John Doe!", doc.GetText().Trim());
```

Montre comment ajouter une mise en forme aux paragraphes dans lesquels une opération de recherche et de remplacement a trouvé des correspondances.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.Writeln("This one will not!");
builder.Write("This one also will.");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(ParagraphAlignment.Left, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[2].ParagraphFormat.Alignment);

// Nous pouvons utiliser un objet « FindReplaceOptions » pour modifier le processus de recherche et de remplacement.
FindReplaceOptions options = new FindReplaceOptions();

// Définissez la propriété « Alignment » sur « ParagraphAlignment.Right » pour aligner à droite chaque paragraphe
// qui contient une correspondance trouvée par l'opération de recherche et de remplacement.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Remplacez chaque point situé juste avant un saut de paragraphe par un point d'exclamation.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

### Voir également

* class [Range](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## Replace(*Regex, string*) {#replace_2}

Remplace toutes les occurrences d'un modèle de caractère spécifié par une expression régulière par une autre chaîne.

```csharp
public int Replace(Regex pattern, string replacement)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| pattern | Regex | Un modèle d'expression régulière utilisé pour trouver des correspondances. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |

### Return_Value

Le nombre de remplacements effectués.

## Remarques

Remplace l'intégralité de la correspondance capturée par l'expression régulière.

La méthode est capable de traiter les ruptures dans les chaînes de modèle et de remplacement.

Vous devez utiliser des méta-caractères spéciaux si vous devez travailler avec des sauts :

* **&amp;p** - saut de paragraphe
* **&amp;b** - saut de section
* **&amp;m** - saut de page
* **&amp;l** - saut de ligne manuel

Utiliser la méthode`Replace` pour avoir une personnalisation plus flexible.

## Exemples

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Remplace chaque numéro par un saut de paragraphe.
doc.Range.Replace(new Regex(@"\d+"), "&p");
```

Montre comment remplacer toutes les occurrences d'un modèle d'expression régulière par un autre texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("I decided to get the curtains in gray, ideal for the grey-accented room.");

doc.Range.Replace(new Regex("gr(a|e)y"), "lavender");

Assert.AreEqual("I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc.GetText().Trim());
```

### Voir également

* class [Range](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## Replace(*string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_1}

Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement.

```csharp
public int Replace(string pattern, string replacement, FindReplaceOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| pattern | String | Une chaîne à remplacer. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objet pour spécifier des options supplémentaires. |

### Return_Value

Le nombre de remplacements effectués.

## Remarques

Le modèle ne sera pas utilisé comme expression régulière. Veuillez utiliser`Replace` si vous avez besoin d'expressions régulières.

La méthode est capable de traiter les ruptures dans les chaînes de modèle et de remplacement.

Vous devez utiliser des méta-caractères spéciaux si vous devez travailler avec des sauts :

* **&amp;p** - saut de paragraphe
* **&amp;b** - saut de section
* **&amp;m** - saut de page
* **&amp;l** - saut de ligne manuel
* **&amp;&amp;** - &amp; personnage

## Exemples

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Insère un saut de paragraphe après Numbers.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Montre comment remplacer du texte dans le pied de page d'un document.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Montre comment basculer la sensibilité à la casse lors de l'exécution d'une opération de recherche et de remplacement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Nous pouvons utiliser un objet « FindReplaceOptions » pour modifier le processus de recherche et de remplacement.
FindReplaceOptions options = new FindReplaceOptions();

// Définissez l'indicateur « MatchCase » sur « true » pour appliquer la sensibilité à la casse lors de la recherche des chaînes à remplacer.
// Définissez l'indicateur « MatchCase » sur « false » pour ignorer la casse des caractères lors de la recherche du texte à remplacer.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Montre comment basculer entre les opérations de recherche et de remplacement de mots autonomes uniquement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Nous pouvons utiliser un objet « FindReplaceOptions » pour modifier le processus de recherche et de remplacement.
FindReplaceOptions options = new FindReplaceOptions();

// Définissez l'indicateur « FindWholeWordsOnly » sur « true » pour remplacer le texte trouvé s'il ne fait pas partie d'un autre mot.
// Définissez l'indicateur « FindWholeWordsOnly » sur « false » pour remplacer tout le texte quel que soit son environnement.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

Montre comment remplacer toutes les instances d'une chaîne de texte dans un tableau et une cellule.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Carrots");
builder.InsertCell();
builder.Write("50");
builder.EndRow();
builder.InsertCell();
builder.Write("Potatoes");
builder.InsertCell();
builder.Write("50");
builder.EndTable();

FindReplaceOptions options = new FindReplaceOptions();
options.MatchCase = true;
options.FindWholeWordsOnly = true;

// Effectuer une opération de recherche et de remplacement sur une table entière.
table.Range.Replace("Carrots", "Eggs", options);

// Effectuez une opération de recherche et de remplacement sur la dernière cellule de la dernière ligne du tableau.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

### Voir également

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## Replace(*Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_3}

Remplace toutes les occurrences d'un modèle de caractère spécifié par une expression régulière par une autre chaîne.

```csharp
public int Replace(Regex pattern, string replacement, FindReplaceOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| pattern | Regex | Un modèle d'expression régulière utilisé pour trouver des correspondances. |
| replacement | String | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objet pour spécifier des options supplémentaires. |

### Return_Value

Le nombre de remplacements effectués.

## Remarques

Remplace l'intégralité de la correspondance capturée par l'expression régulière.

La méthode est capable de traiter les ruptures dans les chaînes de modèle et de remplacement.

Vous devez utiliser des méta-caractères spéciaux si vous devez travailler avec des sauts :

* **&amp;p** - saut de paragraphe
* **&amp;b** - saut de section
* **&amp;m** - saut de page
* **&amp;l** - saut de ligne manuel
* **&amp;&amp;** - &amp; personnage

## Exemples

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Remplace chaque numéro par un saut de paragraphe.
doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
```

Montre comment remplacer toutes les occurrences d'un modèle d'expression régulière par une autre chaîne, tout en suivant tous ces remplacements.

```csharp
public void ReplaceWithCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Nous pouvons utiliser un objet « FindReplaceOptions » pour modifier le processus de recherche et de remplacement.
    FindReplaceOptions options = new FindReplaceOptions();

    // Définissez un rappel qui suit tous les remplacements que la méthode « Remplacer » effectuera.
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Conserve un journal de chaque remplacement de texte effectué par une opération de recherche et de remplacement
/// et note la valeur du texte correspondant d'origine.
/// </summary>
private class TextFindAndReplacementLogger : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        mLog.AppendLine($"\"{args.Match.Value}\" converted to \"{args.Replacement}\" " +
                        $"{args.MatchOffset} characters into a {args.MatchNode.NodeType} node.");

        args.Replacement = $"(Old value:\"{args.Match.Value}\") {args.Replacement}";
        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

Montre comment insérer le contenu entier d'un document en remplacement d'une correspondance dans une opération de recherche et de remplacement.

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Nous pouvons utiliser un objet « FindReplaceOptions » pour modifier le processus de recherche et de remplacement.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

}

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Insérer un document après le paragraphe contenant le texte correspondant.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Supprimez le paragraphe avec le texte correspondant.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Insère tous les nœuds d'un autre document après un paragraphe ou un tableau.
/// </summary>
private static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode dstStory = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                // Ignorer le nœud s'il s'agit du dernier paragraphe vide d'une section.
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                dstStory.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node must be either a paragraph or table.");
    }
}
```

### Voir également

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
