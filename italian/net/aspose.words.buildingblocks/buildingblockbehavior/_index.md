---
title: BuildingBlockBehavior Enum
linktitle: BuildingBlockBehavior
articleTitle: BuildingBlockBehavior
second_title: Aspose.Words per .NET
description: Aspose.Words.BuildingBlocks.BuildingBlockBehavior enum. Specifica il comportamento che deve essere applicato al contenuto del building block quando viene inserito nel documento principale in C#.
type: docs
weight: 140
url: /it/net/aspose.words.buildingblocks/buildingblockbehavior/
---
## BuildingBlockBehavior enumeration

Specifica il comportamento che deve essere applicato al contenuto del building block quando viene inserito nel documento principale.

```csharp
public enum BuildingBlockBehavior
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Content | `0` | Specifica che il blocco predefinito deve essere inserito come contenuto in linea. |
| Paragraph | `1` | Specifica che il blocco predefinito deve essere inserito nel proprio paragrafo. |
| Page | `2` | Specifica che il blocco predefinito verrà aggiunto nella propria pagina. |
| Default | `0` | Uguale aContent . |

## Osservazioni

Corrisponde a**ST_DocPartBehavior** digitare OOXML.

## Esempi

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
