---
title: BuiltInDocumentProperties.Characters
second_title: Référence de l'API Aspose.Words pour .NET
description: BuiltInDocumentProperties propriété. Représente une estimation du nombre de caractères dans le document.
type: docs
weight: 40
url: /fr/net/aspose.words.properties/builtindocumentproperties/characters/
---
## BuiltInDocumentProperties.Characters property

Représente une estimation du nombre de caractères dans le document.

```csharp
public int Characters { get; set; }
```

### Remarques

Aspose.Words met à jour cette propriété lorsque vous appelez[`UpdateWordCount`](../../../aspose.words/document/updatewordcount/).

### Exemples

Montre comment mettre à jour toutes les étiquettes de liste dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words ne suit pas les métriques des documents comme celles-ci en temps réel.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Pour obtenir des valeurs précises pour trois de ces propriétés, nous devrons les mettre à jour manuellement.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Pour le nombre de lignes, nous devrons appeler une surcharge spécifique de la méthode de mise à jour.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

Montre comment utiliser les propriétés du document dans la catégorie « Contenu ».

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // En utilisant les propriétés intégrées,
    // nous pouvons traiter les statistiques du document telles que le nombre de mots/pages/caractères comme des métadonnées pouvant être consultées sans ouvrir le document
    // Ces propriétés sont accessibles en cliquant avec le bouton droit sur le fichier dans l'Explorateur Windows et en accédant à Propriétés > Détails > Contenu
    // Si nous voulons afficher ces données à l'intérieur du document, nous pouvons utiliser des champs tels que NUMPAGES, NUMWORDS, NUMCHARS etc.
    // De plus, ces valeurs peuvent également être affichées dans Microsoft Word en parcourant Fichier > Propriétés > Propriétés avancées > Statistiques
    // Nombre de pages : La propriété PageCount affiche le nombre de pages en temps réel et sa valeur peut être attribuée à la propriété Pages

     // La propriété "Pages" stocke le nombre de pages du document.
    Assert.AreEqual(6, properties.Pages);

    // Les propriétés intégrées "Words", "Characters" et "CharactersWithSpaces" affichent également diverses statistiques de document,
    // mais nous devons appeler la méthode "UpdateWordCount" sur l'ensemble du document avant de pouvoir nous attendre à ce qu'il contienne des valeurs précises.
    doc.UpdateWordCount();

    Assert.AreEqual(1035, properties.Words);
    Assert.AreEqual(6026, properties.Characters);
    Assert.AreEqual(7041, properties.CharactersWithSpaces);

    // Comptez le nombre de lignes dans le document, puis attribuez le résultat à la propriété intégrée "Lines".
    LineCounter lineCounter = new LineCounter(doc);
    properties.Lines = lineCounter.GetLineCount();

    Assert.AreEqual(142, properties.Lines);

    // Attribue le nombre de nœuds de paragraphe dans le document à la propriété intégrée "Paragraphes".
    properties.Paragraphs = doc.GetChildNodes(NodeType.Paragraph, true).Count;
    Assert.AreEqual(29, properties.Paragraphs);

    // Obtenez une estimation de la taille du fichier de notre document via la propriété intégrée "Bytes".
    Assert.AreEqual(20310, properties.Bytes);

    // Définissez un modèle différent pour notre document, puis mettez à jour manuellement la propriété intégrée "Modèle" pour refléter ce changement.
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);    

    properties.Template = doc.AttachedTemplate;

    // "ContentStatus" est une propriété intégrée descriptive.
    properties.ContentStatus = "Draft";

    // Lors de l'enregistrement, la propriété intégrée "ContentType" contiendra le type MIME du format de sauvegarde de sortie.
    Assert.AreEqual(string.Empty, properties.ContentType);

    // Si le document contient des liens, et qu'ils sont tous à jour, nous pouvons définir la propriété "LinksUpToDate" sur "true".
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// Compte les lignes d'un document.
/// Parcourt l'arborescence des entités de mise en page du document lors de la construction,
/// comptage des entités de type "Ligne" contenant également du texte réel.
/// </summary>
private class LineCounter
{
    public LineCounter(Document doc)
    {
        mLayoutEnumerator = new LayoutEnumerator(doc);

        CountLines();
    }

    public int GetLineCount()
    {
        return mLineCount;
    }

    private void CountLines()
    {
        do
        {
            if (mLayoutEnumerator.Type == LayoutEntityType.Line)
            {
                mScanningLineForRealText = true;
            }

            if (mLayoutEnumerator.MoveFirstChild())
            {
                if (mScanningLineForRealText && mLayoutEnumerator.Kind.StartsWith("TEXT"))
                {
                    mLineCount++;
                    mScanningLineForRealText = false;
                }
                CountLines();
                mLayoutEnumerator.MoveParent();
            }
        } while (mLayoutEnumerator.MoveNext());
    }

    private readonly LayoutEnumerator mLayoutEnumerator;
    private int mLineCount;
    private bool mScanningLineForRealText;
}
```

### Voir également

* class [BuiltInDocumentProperties](../)
* espace de noms [Aspose.Words.Properties](../../builtindocumentproperties/)
* Assemblée [Aspose.Words](../../../)


