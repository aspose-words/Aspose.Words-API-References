---
title: ContentStatus
second_title: Référence de l'API Aspose.Words pour .NET
description: Obtient ou définit le ContentStatus du document.
type: docs
weight: 80
url: /fr/net/aspose.words.properties/builtindocumentproperties/contentstatus/
---
## BuiltInDocumentProperties.ContentStatus property

Obtient ou définit le ContentStatus du document.

```csharp
public string ContentStatus { get; set; }
```

### Exemples

Montre comment travailler avec les propriétés du document dans la catégorie "Contenu".

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // En utilisant les propriétés intégrées,
    // nous pouvons traiter les statistiques du document telles que le nombre de mots/pages/caractères comme des métadonnées qui peuvent être consultées sans ouvrir le document
    // Ces propriétés sont accessibles en cliquant avec le bouton droit sur le fichier dans l'Explorateur Windows et en naviguant jusqu'à Propriétés > Détails > Contenu
    // Si nous voulons afficher ces données dans le document, nous pouvons utiliser des champs tels que NUMPAGES, NUMWORDS, NUMCHARS etc.
    // En outre, ces valeurs peuvent également être affichées dans Microsoft Word en naviguant Fichier > Propriétés > Propriétés avancées > Statistiques
    // Nombre de pages : la propriété PageCount affiche le nombre de pages en temps réel et sa valeur peut être affectée à la propriété Pages

    // La propriété "Pages" stocke le nombre de pages du document. 
    Assert.AreEqual(6, properties.Pages);

    // Les propriétés intégrées "Words", "Characters" et "CharactersWithSpaces" affichent également diverses statistiques de document,
    // mais nous devons appeler la méthode "UpdateWordCount" sur l'ensemble du document avant de pouvoir nous attendre à ce qu'ils contiennent des valeurs précises.
    doc.UpdateWordCount();

    Assert.AreEqual(1035, properties.Words);
    Assert.AreEqual(6026, properties.Characters);
    Assert.AreEqual(7041, properties.CharactersWithSpaces);

    // Comptez le nombre de lignes dans le document, puis affectez le résultat à la propriété intégrée "Lignes".
    LineCounter lineCounter = new LineCounter(doc);
    properties.Lines = lineCounter.GetLineCount();

    Assert.AreEqual(142, properties.Lines);

    // Affecte le nombre de nœuds Paragraphe dans le document à la propriété intégrée "Paragraphes".
    properties.Paragraphs = doc.GetChildNodes(NodeType.Paragraph, true).Count;
    Assert.AreEqual(29, properties.Paragraphs);

    // Obtenir une estimation de la taille de fichier de notre document via la propriété intégrée "Bytes".
    Assert.AreEqual(20310, properties.Bytes);

    // Définissez un modèle différent pour notre document, puis mettez à jour manuellement la propriété intégrée "Template" pour refléter ce changement.
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);    

    properties.Template = doc.AttachedTemplate;

    // "ContentStatus" est une propriété intégrée descriptive.
    properties.ContentStatus = "Draft";

    // Lors de l'enregistrement, la propriété intégrée "ContentType" contiendra le type MIME du format d'enregistrement de sortie.
    Assert.AreEqual(string.Empty, properties.ContentType);

    // Si le document contient des liens et qu'ils sont tous à jour, nous pouvons définir la propriété "LinksUpToDate" sur "true".
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// Compte les lignes d'un document.
/// Parcourt l'arborescence des entités de mise en page du document lors de sa construction,
/// comptage des entités de type "Ligne" qui contiennent également du vrai texte.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
