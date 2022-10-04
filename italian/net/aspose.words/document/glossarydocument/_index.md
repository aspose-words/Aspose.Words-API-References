---
title: GlossaryDocument
second_title: Aspose.Words per .NET API Reference
description: Ottiene o imposta il documento del glossario allinterno di questo documento o modello. Un documento di glossario è un archivio per voci di glossario correzione automatica e blocchi predefiniti definiti in un documento.
type: docs
weight: 170
url: /it/net/aspose.words/document/glossarydocument/
---
## Document.GlossaryDocument property

Ottiene o imposta il documento del glossario all'interno di questo documento o modello. Un documento di glossario è un archivio per voci di glossario, correzione automatica e blocchi predefiniti definiti in un documento.

```csharp
public GlossaryDocument GlossaryDocument { get; set; }
```

### Osservazioni

Questa proprietà ritorna`nullo` se il documento non dispone di un documento di glossario.

Puoi aggiungere un documento di glossario a un documento creando a [`GlossaryDocument`](../../../aspose.words.buildingblocks/glossarydocument/) oggetto e assegnando a questa proprietà.

### Esempi

Mostra come aggiungere un blocco predefinito personalizzato a un documento.

```csharp
public void CreateAndInsert()
{
    // Il documento del glossario di un documento memorizza i blocchi costitutivi.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // Crea un building block, assegnagli un nome e quindi aggiungilo al documento del glossario.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // Tutti i nuovi GUID dei blocchi predefiniti hanno lo stesso valore zero per impostazione predefinita e possiamo assegnare loro un nuovo valore univoco.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // Le seguenti proprietà classificano i blocchi predefiniti
    // nel menu possiamo accedere in Microsoft Word tramite "Inserisci" -> "Parti rapide" -> "Organizzatore di blocchi di costruzione".
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Prima di poter aggiungere questo blocco di costruzione al nostro documento, dovremo dargli alcuni contenuti,
    // cosa che faremo usando un visitatore del documento. Questo visitatore imposterà anche una categoria, una galleria e un comportamento.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    block.Accept(visitor);

    // Possiamo accedere al blocco che abbiamo appena creato dal documento del glossario.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // Il blocco stesso è una sezione che contiene il testo.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);

    // Ora possiamo inserirlo nel documento come una nuova sezione.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // Possiamo anche trovarlo nell'organizzatore dei blocchi predefiniti di Microsoft Word e posizionarlo manualmente.
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
        // Configura il building block come parte rapida e aggiungi le proprietà usate da Building Blocks Organizer.
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
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
