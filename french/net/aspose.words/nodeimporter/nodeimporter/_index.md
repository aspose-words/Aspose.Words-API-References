---
title: NodeImporter
second_title: Référence de l'API Aspose.Words pour .NET
description: Initialise une nouvelle instance duNodeImporteraspose.words/nodeimporter/ classe.
type: docs
weight: 10
url: /fr/net/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode) {#constructor}

Initialise une nouvelle instance du[`NodeImporter`](../) classe.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| srcDoc | DocumentBase | Le document source. |
| dstDoc | DocumentBase | Le document de destination qui sera le propriétaire des nœuds importés. |
| importFormatMode | ImportFormatMode | Spécifie comment fusionner les mises en forme de style qui entrent en conflit. |

### Exemples

Montre comment insérer le contenu d'un document dans un signet d'un autre document.

```csharp
[Test]
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

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [NodeImporter](../)
* espace de noms [Aspose.Words](../../nodeimporter/)
* Assemblée [Aspose.Words](../../../)

---

## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) {#constructor_1}

Initialise une nouvelle instance du[`NodeImporter`](../) classe.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| srcDoc | DocumentBase | Le document source. |
| dstDoc | DocumentBase | Le document de destination qui sera le propriétaire des nœuds importés. |
| importFormatMode | ImportFormatMode | Spécifie comment fusionner les mises en forme de style qui entrent en conflit. |
| importFormatOptions | ImportFormatOptions | Spécifie diverses options pour formater le nœud importé. |

### Exemples

Montre comment résoudre un conflit lors de l'importation de documents contenant des listes avec le même identifiant de définition de liste.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Définissez la propriété "KeepSourceNumbering" sur "true" pour appliquer un ID de définition de liste différent
// aux styles identiques car Aspose.Words les importe dans les documents de destination.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

Montre comment résoudre les conflits de numérotation de liste dans les documents source et de destination.

```csharp
// Ouvre un document avec un schéma de numérotation de liste personnalisé, puis le clone.
// Puisque les deux ont le même format de numérotation, les formats entreront en conflit si nous importons un document dans l'autre.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Lorsque nous importons le clone du document dans l'original, puis l'ajoutons,
// alors les deux listes avec le même format de liste se rejoindront.
// Si nous définissons le drapeau "KeepSourceNumbering" sur "false", alors la liste du document clone
// que nous ajoutons à l'original portera la numérotation de la liste à laquelle nous l'ajoutons.
// Cela fusionnera efficacement les deux listes en une seule.
// Si nous définissons le drapeau "KeepSourceNumbering" sur "true", alors le document clone
// list conservera sa numérotation d'origine, faisant apparaître les deux listes comme des listes séparées. 
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.KeepSourceNumbering = keepSourceNumbering;

NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepDifferentStyles, importFormatOptions);
foreach (Paragraph paragraph in srcDoc.FirstSection.Body.Paragraphs)
{
    Node importedNode = importer.ImportNode(paragraph, true);
    dstDoc.FirstSection.Body.AppendChild(importedNode);
}

dstDoc.UpdateListLabels();

if (keepSourceNumbering)
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
else
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
```

### Voir également

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [NodeImporter](../)
* espace de noms [Aspose.Words](../../nodeimporter/)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
