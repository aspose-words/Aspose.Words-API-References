---
title: BuildingBlock.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words per .NET
description: Scopri il metodo Accept di BuildingBlock per coinvolgere i visitatori in modo fluido e migliorare l'esperienza utente. Sfrutta appieno il potenziale del tuo sito web oggi stesso!
type: docs
weight: 130
url: /it/net/aspose.words.buildingblocks/buildingblock/accept/
---
## BuildingBlock.Accept method

Accetta un visitatore.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| visitor | DocumentVisitor | Il visitatore che visiterà i nodi. |

### Valore di ritorno

Vero se tutti i nodi sono stati visitati; falso se[`DocumentVisitor`](../../../aspose.words/documentvisitor/) ha interrotto l'operazione prima di visitare tutti i nodi.

## Osservazioni

Enumera questo nodo e tutti i suoi figli. Ogni nodo chiama un metodo corrispondente su[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Per maggiori informazioni, vedere il design pattern Visitor.

chiamate[`VisitBuildingBlockStart`](../../../aspose.words/documentvisitor/visitbuildingblockstart/) , quindi chiama [`Accept`](../../../aspose.words/node/accept/) per tutti i nodi figlio di questo blocco di costruzione, quindi chiama [`VisitBuildingBlockEnd`](../../../aspose.words/documentvisitor/visitbuildingblockend/).

Nota: un nodo di blocco di costruzione e i suoi figli non vengono visitati quando si esegue un Visitatore su un[`Document`](../../../aspose.words/document/) Se si desidera eseguire un visitatore su un blocco di costruzione , è necessario eseguire il visitatore su[`GlossaryDocument`](../../glossarydocument/) o chiamata`Accept` .

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

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [BuildingBlock](../)
* spazio dei nomi [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* assemblea [Aspose.Words](../../../)
