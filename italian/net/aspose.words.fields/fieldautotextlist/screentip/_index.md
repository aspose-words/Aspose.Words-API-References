---
title: FieldAutoTextList.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: Aspose.Words per .NET
description: FieldAutoTextList ScreenTip proprietà. Ottiene o imposta il testo della descrizione comando da mostrare in C#.
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldautotextlist/screentip/
---
## FieldAutoTextList.ScreenTip property

Ottiene o imposta il testo della descrizione comando da mostrare.

```csharp
public string ScreenTip { get; set; }
```

## Esempi

Mostra come utilizzare un campo AUTOTEXTLIST per selezionare da un elenco di voci di glossario.

```csharp
public void FieldAutoTextList()
{
    Document doc = new Document();

    // Crea un documento di glossario e popolalo con voci di testo automatiche.
    doc.GlossaryDocument = new GlossaryDocument();
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 1", "Contents of AutoText 1");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 2", "Contents of AutoText 2");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 3", "Contents of AutoText 3");

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Crea un campo AUTOTEXTLIST e imposta il testo che verrà visualizzato nel campo in Microsoft Word.
    // Imposta il testo per richiedere all'utente di fare clic con il pulsante destro del mouse su questo campo per selezionare un blocco predefinito di glossario,
    // il cui contenuto verrà visualizzato nel campo.
    FieldAutoTextList field = (FieldAutoTextList)builder.InsertField(FieldType.FieldAutoTextList, true);
    field.EntryName = "Right click here to select an AutoText block";
    field.ListStyle = "Heading 1";
    field.ScreenTip = "Hover tip text for AutoTextList goes here";

    Assert.AreEqual(" AUTOTEXTLIST  \"Right click here to select an AutoText block\" " +
                    "\\s \"Heading 1\" " +
                    "\\t \"Hover tip text for AutoTextList goes here\"", field.GetFieldCode());

    doc.Save(ArtifactsDir + "Field.AUTOTEXTLIST.dotx");
}

/// <summary>
/// Crea un blocco predefinito di tipo Glossario e aggiungilo a un documento di glossario.
/// </summary>
private static void AppendAutoTextEntry(GlossaryDocument glossaryDoc, string name, string contents)
{
    BuildingBlock buildingBlock = new BuildingBlock(glossaryDoc);
    buildingBlock.Name = name;
    buildingBlock.Gallery = BuildingBlockGallery.AutoText;
    buildingBlock.Category = "General";
    buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;

    Section section = new Section(glossaryDoc);
    section.AppendChild(new Body(glossaryDoc));
    section.Body.AppendParagraph(contents);
    buildingBlock.AppendChild(section);

    glossaryDoc.AppendChild(buildingBlock);
}
```

### Guarda anche

* class [FieldAutoTextList](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
