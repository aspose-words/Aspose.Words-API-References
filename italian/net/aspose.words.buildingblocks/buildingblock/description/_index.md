---
title: BuildingBlock.Description
linktitle: Description
articleTitle: Description
second_title: Aspose.Words per .NET
description: Gestisci la descrizione dei tuoi BuildingBlock in tutta semplicità. Imposta o aggiorna facilmente le descrizioni per una migliore organizzazione e chiarezza nei tuoi progetti.
type: docs
weight: 40
url: /it/net/aspose.words.buildingblocks/buildingblock/description/
---
## BuildingBlock.Description property

Ottiene o imposta la descrizione associata a questo blocco di costruzione.

```csharp
public string Description { get; set; }
```

## Osservazioni

La descrizione può contenere qualsiasi tipo di stringa, solitamente informazioni aggiuntive.

Non può essere`null`, ma può essere una stringa vuota.

Corrisponde al**docPartPr.descrizione** elemento in OOXML.

## Esempi

Mostra come aggiungere un blocco di costruzione personalizzato a un documento.

```csharp
public void CreateAndInsert()
{
    // Il glossario di un documento memorizza i componenti fondamentali.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // Crea un blocco di costruzione, assegnagli un nome e aggiungilo al documento del glossario.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // Per impostazione predefinita, tutti i nuovi GUID dei blocchi costitutivi hanno lo stesso valore zero, a cui possiamo assegnare un nuovo valore univoco.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // Le seguenti proprietà categorizzano i blocchi di costruzione
    // nel menu a cui possiamo accedere in Microsoft Word tramite "Inserisci" -> "Parti rapide" -> "Organizzatore di blocchi di costruzione".
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Prima di poter aggiungere questo elemento costitutivo al nostro documento, dovremo fornirgli dei contenuti,
    // che faremo utilizzando un visitatore del documento. Questo visitatore imposterà anche una categoria, una galleria e un comportamento.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    // Visita l'inizio/la fine del BuildingBlock.
    block.Accept(visitor);

    // Possiamo accedere al blocco appena creato dal documento del glossario.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // Il blocco stesso è una sezione che contiene il testo.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);
    // Ora possiamo inserirlo nel documento come nuova sezione.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // Possiamo anche trovarlo nell'Organizzatore dei blocchi di Microsoft Word e posizionarlo manualmente.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// Imposta un blocco di costruzione visitato da inserire nel documento come parte rapida e aggiunge testo al suo contenuto.
/// </summary>
public class BuildingBlockVisitor : DocumentVisitor
{
    public BuildingBlockVisitor(GlossaryDocument ownerGlossaryDoc)
    {
        mBuilder = new StringBuilder();
        mGlossaryDoc = ownerGlossaryDoc;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        // Configura il blocco di costruzione come parte rapida e aggiungi le proprietà utilizzate da Building Blocks Organizer.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // Aggiungi una sezione con testo.
        // L'inserimento del blocco nel documento aggiungerà questa sezione con i suoi nodi figlio nella posizione.
        Section section = new Section(mGlossaryDoc);
        block.AppendChild(section);
        block.FirstSection.EnsureMinimum();

        Run run = new Run(mGlossaryDoc, "Text inside " + block.Name);
        block.FirstSection.Body.FirstParagraph.AppendChild(run);

        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.Append("Visited " + block.Name + "\r\n");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
    private readonly GlossaryDocument mGlossaryDoc;
}
```

### Guarda anche

* class [BuildingBlock](../)
* spazio dei nomi [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* assemblea [Aspose.Words](../../../)
