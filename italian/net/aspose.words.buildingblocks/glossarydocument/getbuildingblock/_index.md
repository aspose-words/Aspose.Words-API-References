---
title: GetBuildingBlock
second_title: Aspose.Words per .NET API Reference
description: Trova un building block utilizzando la galleria la categoria e il nome specificati.
type: docs
weight: 70
url: /it/net/aspose.words.buildingblocks/glossarydocument/getbuildingblock/
---
## GlossaryDocument.GetBuildingBlock method

Trova un building block utilizzando la galleria, la categoria e il nome specificati.

```csharp
public BuildingBlock GetBuildingBlock(BuildingBlockGallery gallery, string category, string name)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| gallery | BuildingBlockGallery | I criteri della galleria. |
| category | String | I criteri di categoria. Può essere nullo, nel qual caso non verrà utilizzato per il confronto. |
| name | String | I criteri del nome del blocco predefinito. |

### Valore di ritorno

Il blocco predefinito corrispondente o null se non è stata trovata una corrispondenza.

### Osservazioni

Questo è un metodo pratico che esegue l'iterazione su tutti i building block in questa raccolta e restituisce il primo building block che corrisponde a la galleria, la categoria e il nome specificati.

Microsoft Word organizza i blocchi costitutivi in gallerie. Le gallerie sono predefinite utilizzando il[`BuildingBlockGallery`](../../buildingblockgallery/) enum. All'interno di ogni galleria, i blocchi predefiniti possono essere organizzati in una o più categorie. Il nome della categoria è una stringa. Ogni blocco ha un nome. Non è garantito che un nome building block sia univoco.

### Esempi

Mostra le modalità di accesso ai blocchi predefiniti in un documento di glossario.

```csharp
public void GlossaryDocument()
{
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();

    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 1" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 2" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 3" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 4" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 5" });

    Assert.AreEqual(5, glossaryDoc.BuildingBlocks.Count);

    doc.GlossaryDocument = glossaryDoc;

    // Esistono vari modi per accedere ai blocchi predefiniti.
    // 1 - Ottieni i primi/ultimi blocchi di costruzione della collezione:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Ottieni un building block per indice:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - Ottieni il primo building block che corrisponde a una galleria, un nome e una categoria:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Lo faremo utilizzando un visitatore personalizzato,
    // che darà a ogni BuildingBlock nel GlossaryDocument un GUID univoco
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    glossaryDoc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // In Microsoft Word, possiamo accedere ai blocchi predefiniti tramite "Inserisci" -> "Parti rapide" -> "Organizzatore di blocchi di costruzione".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Fornisce a ciascun elemento costitutivo in un documento del glossario visitato un GUID univoco.
/// Memorizza le coppie di blocchi GUID in un dizionario.
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
* spazio dei nomi [Aspose.Words.BuildingBlocks](../../glossarydocument/)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
