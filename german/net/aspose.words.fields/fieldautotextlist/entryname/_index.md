---
title: FieldAutoTextList.EntryName
linktitle: EntryName
articleTitle: EntryName
second_title: Aspose.Words für .NET
description: FieldAutoTextList EntryName eigendom. Ruft den Namen des AutoTextEintrags ab oder legt ihn fest in C#.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldautotextlist/entryname/
---
## FieldAutoTextList.EntryName property

Ruft den Namen des AutoText-Eintrags ab oder legt ihn fest.

```csharp
public string EntryName { get; set; }
```

## Beispiele

Zeigt, wie ein AUTOTEXTLIST-Feld verwendet wird, um aus einer Liste von AutoText-Einträgen auszuwählen.

```csharp
public void FieldAutoTextList()
{
    Document doc = new Document();

    // Ein Glossardokument erstellen und es mit automatischen Texteinträgen füllen.
    doc.GlossaryDocument = new GlossaryDocument();
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 1", "Contents of AutoText 1");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 2", "Contents of AutoText 2");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 3", "Contents of AutoText 3");

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Erstellen Sie ein AUTOTEXTLIST-Feld und legen Sie den Text fest, den das Feld in Microsoft Word anzeigen soll.
    // Legen Sie den Text so fest, dass der Benutzer aufgefordert wird, mit der rechten Maustaste auf dieses Feld zu klicken, um einen AutoText-Baustein auszuwählen.
    // dessen Inhalt das Feld anzeigt.
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
/// Erstellen Sie einen Baustein vom Typ AutoText und fügen Sie ihn einem Glossardokument hinzu.
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

### Siehe auch

* class [FieldAutoTextList](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
