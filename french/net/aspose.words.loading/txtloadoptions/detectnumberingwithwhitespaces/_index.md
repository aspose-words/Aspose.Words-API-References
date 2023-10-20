---
title: TxtLoadOptions.DetectNumberingWithWhitespaces
linktitle: DetectNumberingWithWhitespaces
articleTitle: DetectNumberingWithWhitespaces
second_title: Aspose.Words pour .NET
description: TxtLoadOptions DetectNumberingWithWhitespaces propriété. Permet de spécifier comment les éléments de liste numérotés sont reconnus lorsque le document est importé à partir du format texte brut. La valeur par défaut estvrai en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/
---
## TxtLoadOptions.DetectNumberingWithWhitespaces property

Permet de spécifier comment les éléments de liste numérotés sont reconnus lorsque le document est importé à partir du format texte brut. La valeur par défaut est`vrai`.

```csharp
public bool DetectNumberingWithWhitespaces { get; set; }
```

## Remarques

Si cette option est définie sur`FAUX`, l'algorithme de reconnaissance de listes détecte les paragraphes de liste lorsque les numéros de liste se terminent par soit par un point, soit par un crochet droit, soit par des puces (tels que "•", "*", "-" ou "o").

Si cette option est définie sur`vrai`les espaces sont également utilisés comme délimiteurs de numéros de liste : l'algorithme de reconnaissance de liste pour la numérotation de style arabe (1., 1.1.2.) utilise à la fois les espaces et les symboles point ("").

## Exemples

Montre comment détecter les listes lors du chargement de documents en texte brut.

```csharp
// Crée un document en texte brut dans une chaîne avec quatre parties distinctes que l'on peut interpréter comme des listes,
// avec des délimiteurs différents. Lors du chargement du document en clair dans un objet "Document",
// Aspose.Words détectera toujours les trois premières listes et ajoutera un objet "List"
// pour chacun à la propriété "Listes" du document.
const string textDoc = "Full stop delimiters:\n" +
                       "1. First list item 1\n" +
                       "2. First list item 2\n" +
                       "3. First list item 3\n\n" +
                       "Right bracket delimiters:\n" +
                       "1) Second list item 1\n" +
                       "2) Second list item 2\n" +
                       "3) Second list item 3\n\n" +
                       "Bullet delimiters:\n" +
                       "• Third list item 1\n" +
                       "• Third list item 2\n" +
                       "• Third list item 3\n\n" +
                       "Whitespace delimiters:\n" +
                       "1 Fourth list item 1\n" +
                       "2 Fourth list item 2\n" +
                       "3 Fourth list item 3";

// Crée un objet "TxtLoadOptions", que l'on peut transmettre au constructeur d'un document
// pour modifier la façon dont nous chargeons un document en texte brut.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Définit la propriété "DetectNumberingWithWhitespaces" sur "true" pour détecter les éléments numérotés
// avec des délimiteurs d'espaces, comme la quatrième liste de notre document, sous forme de listes.
// Cela peut également détecter à tort les paragraphes commençant par des chiffres sous forme de listes.
// Définit la propriété "DetectNumberingWithWhitespaces" sur "false"
// pour ne pas créer de listes à partir d'éléments numérotés avec des délimiteurs d'espaces.
loadOptions.DetectNumberingWithWhitespaces = detectNumberingWithWhitespaces;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(textDoc)), loadOptions);

if (detectNumberingWithWhitespaces)
{
    Assert.AreEqual(4, doc.Lists.Count);
    Assert.True(doc.FirstSection.Body.Paragraphs.Any(p => p.GetText().Contains("Fourth list") && ((Paragraph)p).IsListItem));
}
else
{
    Assert.AreEqual(3, doc.Lists.Count);
    Assert.False(doc.FirstSection.Body.Paragraphs.Any(p => p.GetText().Contains("Fourth list") && ((Paragraph)p).IsListItem));
}
```

### Voir également

* class [TxtLoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
