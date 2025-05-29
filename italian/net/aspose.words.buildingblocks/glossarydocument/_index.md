---
title: GlossaryDocument Class
linktitle: GlossaryDocument
articleTitle: GlossaryDocument
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.BuildingBlocks.GlossaryDocument, la chiave per gestire in modo fluido AutoText e Building Blocks nei documenti Word.
type: docs
weight: 370
url: /it/net/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class

Rappresenta l'elemento radice di un documento di glossario all'interno di un documento Word. Un documento di glossario è un archivio per voci di testo automatico, di correzione automatica e blocchi predefiniti.

Per saperne di più, visita il[Modello a oggetti del documento (DOM) di Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) articolo di documentazione.

```csharp
public class GlossaryDocument : DocumentBase
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [GlossaryDocument](glossarydocument/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BackgroundShape](../../aspose.words/documentbase/backgroundshape/) { get; set; } | Ottiene o imposta la forma dello sfondo del documento. Può essere`null` . |
| [BuildingBlocks](../../aspose.words.buildingblocks/glossarydocument/buildingblocks/) { get; } | Restituisce una raccolta tipizzata che rappresenta tutti i blocchi costitutivi nel documento del glossario. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ottiene il numero di figli immediati di questo nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Specifica l'identificatore del nodo personalizzato. |
| override [Document](../../aspose.words/documentbase/document/) { get; } | Ottiene questa istanza. |
| [FirstBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/firstbuildingblock/) { get; } | Ottiene il primo blocco di costruzione nel documento del glossario. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ottiene il primo figlio del nodo. |
| [FontInfos](../../aspose.words/documentbase/fontinfos/) { get; } | Fornisce l'accesso alle proprietà dei font utilizzati in questo documento. |
| [FootnoteSeparators](../../aspose.words/documentbase/footnoteseparators/) { get; } | Fornisce l'accesso ai separatori di note a piè di pagina/note di chiusura definiti nel documento. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Restituisce`VERO` se questo nodo ha nodi figlio. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Restituisce`VERO` poiché questo nodo può avere nodi figlio. |
| [LastBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/lastbuildingblock/) { get; } | Ottiene l'ultimo blocco di costruzione nel documento del glossario. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ottiene l'ultimo figlio del nodo. |
| [Lists](../../aspose.words/documentbase/lists/) { get; } | Fornisce l'accesso alla formattazione dell'elenco utilizzata nel documento. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ottiene il nodo immediatamente successivo a questo nodo. |
| [NodeChangingCallback](../../aspose.words/documentbase/nodechangingcallback/) { get; set; } | Chiamato quando un nodo viene inserito o rimosso nel documento. |
| override [NodeType](../../aspose.words.buildingblocks/glossarydocument/nodetype/) { get; } | Restituisce ilGlossaryDocument valore. |
| [PageColor](../../aspose.words/documentbase/pagecolor/) { get; set; } | Ottiene o imposta il colore della pagina del documento. Questa proprietà è una versione semplificata di[`BackgroundShape`](../../aspose.words/documentbase/backgroundshape/) . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ottiene il genitore immediato di questo nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ottiene il nodo immediatamente precedente questo nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Restituisce un[`Range`](../../aspose.words/range/)oggetto che rappresenta la porzione di un documento contenuta in questo nodo. |
| [ResourceLoadingCallback](../../aspose.words/documentbase/resourceloadingcallback/) { get; set; } | Consente di controllare come vengono caricate le risorse esterne. |
| [Styles](../../aspose.words/documentbase/styles/) { get; } | Restituisce una raccolta di stili definiti nel documento. |
| [WarningCallback](../../aspose.words/documentbase/warningcallback/) { get; set; } | Chiamato durante varie procedure di elaborazione dei documenti quando viene rilevato un problema che potrebbe causare una perdita di fedeltà dei dati o della formattazione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/glossarydocument/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore. |
| override [AcceptEnd](../../aspose.words.buildingblocks/glossarydocument/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore per aver visitato la fine del documento del Glossario. |
| override [AcceptStart](../../aspose.words.buildingblocks/glossarydocument/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Accetta un visitatore per aver visitato l'inizio del documento del Glossario. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Aggiunge il nodo specificato alla fine dell'elenco dei nodi figlio per questo nodo. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Crea un duplicato del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ottiene il primo antenato dell'oggetto specificato[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ottiene il primo antenato del tipo di oggetto specificato. |
| [GetBuildingBlock](../../aspose.words.buildingblocks/glossarydocument/getbuildingblock/)(*[BuildingBlockGallery](../buildingblockgallery/), string, string*) | Trova un elemento costitutivo utilizzando la galleria, la categoria e il nome specificati. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Restituisce un N-esimo nodo figlio che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Restituisce una raccolta live di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Fornisce supporto per ogni iterazione di stile sui nodi figlio di questo nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../../aspose.words/node/), bool*) | Importa un nodo da un altro documento al documento corrente. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(*[Node](../../aspose.words/node/), bool, [ImportFormatMode](../../aspose.words/importformatmode/)*) | Importa un nodo da un altro documento nel documento corrente con un'opzione per controllare la formattazione. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Restituisce l'indice del nodo figlio specificato nell'array dei nodi figlio. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Inserisce il nodo specificato subito dopo il nodo di riferimento specificato. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Inserisce il nodo specificato immediatamente prima del nodo di riferimento specificato. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ottiene il nodo successivo in base all'algoritmo di attraversamento dell'albero preordinato. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Aggiunge il nodo specificato all'inizio dell'elenco dei nodi figlio per questo nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero preordinato. |
| [Remove](../../aspose.words/node/remove/)() | Si rimuove dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Rimuove il nodo figlio specificato. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutto[`SmartTag`](../../aspose.words.markup/smarttag/) nodi discendenti del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Seleziona il primo[`Node`](../../aspose.words/node/) che corrisponde all'espressione XPath. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Esporta il contenuto del nodo in una stringa utilizzando le opzioni di salvataggio specificate. |

## Osservazioni

Alcuni documenti, solitamente modelli, possono contenere voci di testo automatico, voci di correzione automatica e/o blocchi predefiniti (noti anche comevoci del documento del glossario ,parti del documento oblocchi di costruzione).

Per accedere ai blocchi di costruzione, è necessario caricare un documento in un[`Document`](../../aspose.words/document/) Oggetto . I blocchi di costruzione saranno disponibili tramite[`GlossaryDocument`](../../aspose.words/document/glossarydocument/) proprietà.

`GlossaryDocument` può contenere un numero qualsiasi di[`BuildingBlock`](../buildingblock/)oggetti. Ciascuno[`BuildingBlock`](../buildingblock/) rappresenta una parte del documento.

Corrisponde al**glossarioDocumento** E**docParts**elementi in OOXML.

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

* class [DocumentBase](../../aspose.words/documentbase/)
* spazio dei nomi [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* assemblea [Aspose.Words](../../)
