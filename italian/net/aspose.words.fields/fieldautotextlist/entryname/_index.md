---
title: FieldAutoTextList.EntryName
linktitle: EntryName
articleTitle: EntryName
second_title: Aspose.Words per .NET
description: Scopri come gestire le voci di testo automatico con la proprietà FieldAutoTextList EntryName: imposta o recupera facilmente i nomi per una modifica semplificata dei documenti.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldautotextlist/entryname/
---
## FieldAutoTextList.EntryName property

Ottiene o imposta il nome della voce di testo automatico.

```csharp
public string EntryName { get; set; }
```

## Esempi

Mostra come utilizzare un campo AUTOTEXTLIST per selezionare da un elenco di voci di testo automatico.

```csharp
public void FieldAutoTextList()
{
    Document doc = new Document();

    // Crea un documento di glossario e inserisci al suo interno voci di testo automatiche.
    doc.GlossaryDocument = new GlossaryDocument();
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 1", "Contents of AutoText 1");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 2", "Contents of AutoText 2");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 3", "Contents of AutoText 3");

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Crea un campo AUTOTEXTLIST e imposta il testo che il campo visualizzerà in Microsoft Word.
    // Imposta il testo per richiedere all'utente di fare clic con il pulsante destro del mouse su questo campo per selezionare un blocco di creazione di testo automatico,
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
/// Creare un blocco di costruzione di tipo AutoText e aggiungerlo a un documento di glossario.
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
