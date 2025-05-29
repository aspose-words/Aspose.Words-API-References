---
title: GlossaryDocument.GetBuildingBlock
linktitle: GetBuildingBlock
articleTitle: GetBuildingBlock
second_title: Aspose.Words per .NET
description: Scopri il metodo GetBuildingBlock di GlossaryDocument per individuare in modo efficiente i blocchi di costruzione per categoria e nome della galleria. Migliora la tua gestione dei documenti oggi stesso!
type: docs
weight: 90
url: /it/net/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument.GetBuildingBlock method

Trova un elemento costitutivo utilizzando la galleria, la categoria e il nome specificati.

```csharp
public BuildingBlock GetBuildingBlock(BuildingBlockGallery gallery, string category, string name)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| gallery | BuildingBlockGallery | I criteri della galleria. |
| category | String | I criteri di categoria. Possono essere`null`, nel qual caso non verrà utilizzato per il confronto. |
| name | String | Criteri per il nome del blocco di costruzione. |

### Valore di ritorno

Il blocco di costruzione corrispondente o`null` se non è stata trovata alcuna corrispondenza.

## Osservazioni

Si tratta di un metodo pratico che esegue un'iterazione su tutti i blocchi predefiniti in questa raccolta e restituisce il primo blocco predefinito che corrisponde alla galleria, alla categoria e al nome specificati.

Microsoft Word organizza i blocchi di costruzione in gallerie. Le gallerie sono predefinite utilizzando[`BuildingBlockGallery`](../../buildingblockgallery/)enum. All'interno di ogni galleria, i blocchi costitutivi possono essere organizzati in una o più categorie. Il nome della categoria è una stringa. Ogni blocco costitutivo ha un nome. Non è garantito che il nome di un blocco costitutivo sia univoco.

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

* class [BuildingBlock](../../buildingblock/)
* enum [BuildingBlockGallery](../../buildingblockgallery/)
* class [GlossaryDocument](../)
* spazio dei nomi [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* assemblea [Aspose.Words](../../../)
