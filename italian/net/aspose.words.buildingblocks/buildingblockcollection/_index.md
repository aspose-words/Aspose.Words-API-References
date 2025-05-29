---
title: BuildingBlockCollection Class
linktitle: BuildingBlockCollection
articleTitle: BuildingBlockCollection
second_title: Aspose.Words per .NET
description: Scopri la classe BuildingBlockCollection di Aspose.Words, un potente strumento per gestire in modo efficiente gli oggetti BuildingBlock dei documenti e migliorare il flusso di lavoro.
type: docs
weight: 340
url: /it/net/aspose.words.buildingblocks/buildingblockcollection/
---
## BuildingBlockCollection class

Una raccolta di[`BuildingBlock`](../buildingblock/) oggetti nel documento.

Per saperne di più, visita il[Modello a oggetti del documento (DOM) di Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) articolo di documentazione.

```csharp
public class BuildingBlockCollection : NodeCollection
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Ottiene il numero di nodi nella raccolta. |
| [Item](../../aspose.words.buildingblocks/buildingblockcollection/item/) { get; } | Recupera un blocco di costruzione all'indice specificato. (2 indexers) |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../../aspose.words/node/)*) | Aggiunge un nodo alla fine della raccolta. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Rimuove tutti i nodi da questa raccolta e dal documento. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../../aspose.words/node/)*) | Determina se un nodo è nella raccolta. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Fornisce una semplice iterazione in stile "foreach" sulla raccolta di nodi. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../../aspose.words/node/)*) | Restituisce l'indice basato su zero del nodo specificato. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../../aspose.words/node/)*) | Inserisce un nodo nella raccolta all'indice specificato. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../../aspose.words/node/)*) | Rimuove il nodo dalla raccolta e dal documento. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Rimuove il nodo all'indice specificato dalla raccolta e dal documento. |
| [ToArray](../../aspose.words.buildingblocks/buildingblockcollection/toarray/#toarray)() | Copia tutti i blocchi costitutivi dalla raccolta in un nuovo array di blocchi costitutivi. (2 methods) |

## Osservazioni

Non è possibile creare istanze di questa classe direttamente. Per accedere a una raccolta di blocchi di costruzione, utilizzare[`BuildingBlocks`](../glossarydocument/buildingblocks/) proprietà.

## Esempi

Mostra i modi per accedere ai blocchi di costruzione in un documento di glossario.

```csharp
public void GlossaryDocument()
{
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();

    BuildingBlock child1 = new BuildingBlock(glossaryDoc) { Name = "Block 1" };
    glossaryDoc.AppendChild(child1);
    BuildingBlock child2 = new BuildingBlock(glossaryDoc) { Name = "Block 2" };
    glossaryDoc.AppendChild(child2);
    BuildingBlock child3 = new BuildingBlock(glossaryDoc) { Name = "Block 3" };
    glossaryDoc.AppendChild(child3);
    BuildingBlock child4 = new BuildingBlock(glossaryDoc) { Name = "Block 4" };
    glossaryDoc.AppendChild(child4);
    BuildingBlock child5 = new BuildingBlock(glossaryDoc) { Name = "Block 5" };
    glossaryDoc.AppendChild(child5);

    Assert.AreEqual(5, glossaryDoc.BuildingBlocks.Count);

    doc.GlossaryDocument = glossaryDoc;

    // Esistono vari modi per accedere ai componenti di base.
    // 1 - Ottieni i primi/ultimi blocchi costitutivi della raccolta:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Ottieni un blocco di costruzione tramite l'indice:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - Ottieni il primo blocco di costruzione che corrisponde a una galleria, un nome e una categoria:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Lo faremo utilizzando un visitatore personalizzato,
    // che darà a ogni BuildingBlock nel GlossaryDocument un GUID univoco
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    // Visita l'inizio/la fine del documento Glossario.
    glossaryDoc.Accept(visitor);
    // Visita solo l'inizio del documento Glossario.
    glossaryDoc.AcceptStart(visitor);
    // Visita solo la fine del documento Glossario.
    glossaryDoc.AcceptEnd(visitor);
    Console.WriteLine(visitor.GetText());

    // In Microsoft Word, possiamo accedere ai blocchi di costruzione tramite "Inserisci" -> "Parti rapide" -> "Organizzatore blocchi di costruzione".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Assegna a ciascun elemento costitutivo di un documento di glossario visitato un GUID univoco.
/// Memorizza le coppie di blocchi costitutivi GUID in un dizionario.
/// </summary>
public class GlossaryDocVisitor : DocumentVisitor
{
    public GlossaryDocVisitor()
    {
        mBlocksByGuid = new Dictionary<Guid, BuildingBlock>();
        mBuilder = new StringBuilder();
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    public Dictionary<Guid, BuildingBlock> GetDictionary()
    {
        return mBlocksByGuid;
    }

    public override VisitorAction VisitGlossaryDocumentStart(GlossaryDocument glossary)
    {
        mBuilder.AppendLine("Glossary document found!");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitGlossaryDocumentEnd(GlossaryDocument glossary)
    {
        mBuilder.AppendLine("Reached end of glossary!");
        mBuilder.AppendLine("BuildingBlocks found: " + mBlocksByGuid.Count);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        block.Guid = Guid.NewGuid();
        mBlocksByGuid.Add(block.Guid, block);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.AppendLine("\tVisited block \"" + block.Name + "\"");
        mBuilder.AppendLine("\t Type: " + block.Type);
        mBuilder.AppendLine("\t Gallery: " + block.Gallery);
        mBuilder.AppendLine("\t Behavior: " + block.Behavior);
        mBuilder.AppendLine("\t Description: " + block.Description);

        return VisitorAction.Continue;
    }

    private readonly Dictionary<Guid, BuildingBlock> mBlocksByGuid;
    private readonly StringBuilder mBuilder;
}
```

### Guarda anche

* class [NodeCollection](../../aspose.words/nodecollection/)
* spazio dei nomi [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* assemblea [Aspose.Words](../../)
