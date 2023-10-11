---
title: Enum BuildingBlockType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.BuildingBlocks.BuildingBlockType enum. Specifica un tipo di blocco predefinito. Il tipo potrebbe influire sulla visibilità e sul comportamento del blocco predefinito in Microsoft Word.
type: docs
weight: 170
url: /it/net/aspose.words.buildingblocks/buildingblocktype/
---
## BuildingBlockType enumeration

Specifica un tipo di blocco predefinito. Il tipo potrebbe influire sulla visibilità e sul comportamento del blocco predefinito in Microsoft Word.

```csharp
public enum BuildingBlockType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Nessuna informazione sul tipo specificata per il blocco predefinito. |
| AutomaticallyReplaceNameWithContent | `1` | Consente l'inserimento automatico del blocco predefinito nel documento ogni volta che il suo nome viene inserito in un'applicazione. |
| StructuredDocumentTagPlaceholderText | `2` | L'elemento costitutivo è un testo segnaposto tag documento strutturato. |
| FormFieldHelpText | `3` | L'elemento costitutivo è un testo di aiuto per il campo modulo. |
| Normal | `4` | L'elemento costitutivo è una normale (cioè regolare) voce di documento del glossario. |
| AutoCorrect | `5` | Il blocco predefinito è associato agli strumenti di ortografia e grammatica. |
| AutoText | `6` | L'elemento costitutivo è una voce di glossario. |
| All | `7` | Il blocco predefinito è associato a tutti i tipi. |
| Default | `0` | Salva con nomeNone . |

### Osservazioni

Corrisponde a **ST_DocPartType** digitare OOXML.

### Esempi

Mostra come aggiungere un blocco predefinito personalizzato a un documento.

```csharp
public void CreateAndInsert()
{
    // Il documento del glossario di un documento memorizza gli elementi costitutivi.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // Crea un blocco predefinito, assegnagli un nome e quindi aggiungilo al documento del glossario.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // Tutti i nuovi GUID dei blocchi predefiniti hanno lo stesso valore zero per impostazione predefinita e possiamo assegnare loro un nuovo valore univoco.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // Le seguenti proprietà classificano i blocchi predefiniti
    // nel menu a cui possiamo accedere in Microsoft Word tramite "Inserisci" -> "Parti rapide" -> "Organizzatore di blocchi di costruzione" .
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Prima di poter aggiungere questo elemento costitutivo al nostro documento, dovremo dargli alcuni contenuti,
    // cosa che faremo utilizzando un visitatore del documento. Questo visitatore imposterà anche una categoria, una galleria e un comportamento.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    block.Accept(visitor);

    // Possiamo accedere al blocco che abbiamo appena creato dal documento glossario.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // Il blocco stesso è una sezione che contiene il testo.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);
    // Ora possiamo inserirlo nel documento come una nuova sezione.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // Possiamo anche trovarlo nell'Organizzatore dei blocchi di costruzione di Microsoft Word e posizionarlo manualmente.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// Imposta un blocco predefinito visitato da inserire nel documento come parte rapida e aggiunge testo al suo contenuto.
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
        // Configura il building block come parte rapida e aggiunge le proprietà utilizzate da Building Blocks Organizer.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // Aggiunge una sezione con testo.
        // L'inserimento del blocco nel documento aggiungerà questa sezione con i suoi nodi secondari nella posizione.
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

* spazio dei nomi [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* assemblea [Aspose.Words](../../)


