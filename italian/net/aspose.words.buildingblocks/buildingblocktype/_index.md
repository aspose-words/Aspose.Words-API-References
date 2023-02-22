---
title: Enum BuildingBlockType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.BuildingBlocks.BuildingBlockType enum. Specifica un tipo di blocco predefinito. Il tipo potrebbe influire sulla visibilità e sul comportamento del building block in Microsoft Word.
type: docs
weight: 160
url: /it/net/aspose.words.buildingblocks/buildingblocktype/
---
## BuildingBlockType enumeration

Specifica un tipo di blocco predefinito. Il tipo potrebbe influire sulla visibilità e sul comportamento del building block in Microsoft Word.

```csharp
public enum BuildingBlockType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Nessuna informazione sul tipo è specificata per il building block. |
| AutomaticallyReplaceNameWithContent | `1` | Consente l'inserimento automatico del building block nel documento ogni volta che viene immesso il suo nome in un'applicazione. |
| StructuredDocumentTagPlaceholderText | `2` | Il building block è un testo segnaposto di tag documento strutturato. |
| FormFieldHelpText | `3` | Il building block è un testo della guida di un campo modulo. |
| Normal | `4` | Il blocco di costruzione è una voce di documento del glossario normale (cioè regolare). |
| AutoCorrect | `5` | Il blocco predefinito è associato agli strumenti di ortografia e grammatica. |
| AutoText | `6` | Il blocco predefinito è una voce di glossario. |
| All | `7` | Il building block è associato a tutti i tipi. |
| Default | `0` | Salva con nomeNone . |

### Osservazioni

Corrisponde al **ST_DocPartType** digita OOXML.

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

* spazio dei nomi [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* assemblea [Aspose.Words](../../)


