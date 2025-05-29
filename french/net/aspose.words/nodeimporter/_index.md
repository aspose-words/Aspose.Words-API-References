---
title: NodeImporter Class
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: Aspose.Words pour .NET
description: Transférez facilement des nœuds de documents avec Aspose.Words.NodeImporter. Optimisez votre flux de travail et optimisez votre gestion documentaire dès aujourd'hui !
type: docs
weight: 4900
url: /fr/net/aspose.words/nodeimporter/
---
## NodeImporter class

Permet d'effectuer efficacement l'importation répétée de nœuds d'un document à un autre.

Pour en savoir plus, visitez le[Modèle d'objet de document (DOM) Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) article de documentation.

```csharp
public class NodeImporter
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/)*) | Initialise une nouvelle instance du`NodeImporter` classe. |
| [NodeImporter](nodeimporter/#constructor_1)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | Initialise une nouvelle instance du`NodeImporter` classe. |

## Méthodes

| Nom | La description |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(*[Node](../node/), bool*) | Importe un nœud d'un document dans un autre. |

## Remarques

Aspose.Words offre une fonctionnalité permettant de copier et de déplacer facilement des fragments entre des documents Microsoft Word. Cette opération est appelée « importation de nœuds ». Avant d'insérer un fragment d'un document dans un autre, vous devez l'« importer ». L'importation crée un clone complet du nœud d'origine, prêt à être inséré dans le document de destination.

La manière la plus simple d’importer un nœud est d’utiliser le[`ImportNode`](../documentbase/importnode/) method fourni par le[`DocumentBase`](../documentbase/) objet.

Cependant, lorsque vous devez importer des nœuds d'un document à un autre plusieurs fois, il est préférable d'utiliser le`NodeImporter` classe. Le`NodeImporter` La classe permet de minimiser le nombre de styles et de listes créés dans le document de destination.

Copier ou déplacer des fragments d'un document Microsoft Word vers un autre présente de nombreux défis techniques pour Aspose.Words. Dans un document Word, les styles et la mise en forme des listes sont stockés de manière centralisée, séparément du texte. Les paragraphes et les passages de texte font simplement référence aux styles par des identifiants uniques internes.

Les défis proviennent du fait que les styles et les listes sont différents dans différents documents. Par exemple, pour copier un paragraphe formaté avec le style Titre 1 d'un document à un autre, un certain nombre de choses doivent être prises en compte : décider s'il faut copier le style Titre 1 du document source vers le document de destination, cloner le paragraphe, mettre à jour le paragraphe cloné afin qu'il fasse référence au style Titre 1 correct dans le document de destination. Si le style devait être copié, tous les styles auxquels il fait référence (en fonction du style et du style du paragraphe suivant) devraient être analysés et éventuellement copiés également, et ainsi de suite. Des problèmes similaires existent lors de la copie de paragraphes à puces ou numérotés, car Microsoft Word stocke les définitions de liste séparément du texte.

Le`NodeImporter`La classe est comme un contexte, qui contient les tables de traduction lors de l'importation. Elle traduit correctement les styles et les listes des documents source et cible.

## Exemples

Montre comment insérer le contenu d'un document dans un signet d'un autre document.

```csharp
public void InsertAtBookmark()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("InsertionPoint");
    builder.Write("We will insert a document here: ");
    builder.EndBookmark("InsertionPoint");

    Document docToInsert = new Document();
    builder = new DocumentBuilder(docToInsert);

    builder.Write("Hello world!");

    docToInsert.Save(ArtifactsDir + "NodeImporter.InsertAtMergeField.docx");

    Bookmark bookmark = doc.Range.Bookmarks["InsertionPoint"];
    InsertDocument(bookmark.BookmarkStart.ParentNode, docToInsert);

    Assert.AreEqual("We will insert a document here: " +
                    "\rHello world!", doc.GetText().Trim());
}

/// <summary>
/// Insère le contenu d'un document après le nœud spécifié.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // Boucle sur tous les nœuds de niveau bloc dans le corps de la section,
        // puis clonez et insérez chaque nœud qui n'est pas le dernier paragraphe vide d'une section.
        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                destinationParent.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node should be either a paragraph or table.");
    }
}
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
