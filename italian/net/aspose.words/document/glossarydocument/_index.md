---
title: Document.GlossaryDocument
linktitle: GlossaryDocument
articleTitle: GlossaryDocument
second_title: Aspose.Words per .NET
description: Scopri come gestire efficacemente il glossario dei tuoi documenti. Impara a impostare e recuperare le voci di glossario per AutoText e Building Blocks nei tuoi modelli.
type: docs
weight: 180
url: /it/net/aspose.words/document/glossarydocument/
---
## Document.GlossaryDocument property

Ottiene o imposta il documento di glossario all'interno di questo documento o modello. Un documento di glossario è un archivio per le voci di Testo automatico, Correzione automatica e Building Block definite in un documento.

```csharp
public GlossaryDocument GlossaryDocument { get; set; }
```

## Osservazioni

Questa proprietà restituisce`null` se il documento non ha un documento di glossario.

È possibile aggiungere un documento di glossario a un documento creando a [`GlossaryDocument`](../../../aspose.words.buildingblocks/glossarydocument/) oggetto e assegnandolo a questa proprietà.

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

* class [GlossaryDocument](../../../aspose.words.buildingblocks/glossarydocument/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
