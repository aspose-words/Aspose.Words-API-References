---
title: FieldAutoTextList.EntryName
linktitle: EntryName
articleTitle: EntryName
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie AutoText-Einträge mit der Eigenschaft „FieldAutoTextList EntryName“ verwalten – legen Sie Namen einfach fest oder rufen Sie sie ab, um die Dokumentbearbeitung zu optimieren.
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

Zeigt, wie Sie mithilfe eines AUTOTEXTLIST-Felds aus einer Liste mit AutoText-Einträgen auswählen.

```csharp
public void FieldAutoTextList()
{
    Document doc = new Document();

    // Erstellen Sie ein Glossardokument und füllen Sie es mit automatischen Texteinträgen.
    doc.GlossaryDocument = new GlossaryDocument();
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 1", "Contents of AutoText 1");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 2", "Contents of AutoText 2");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 3", "Contents of AutoText 3");

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Erstellen Sie ein AUTOTEXTLIST-Feld und legen Sie den Text fest, der im Feld in Microsoft Word angezeigt wird.
    // Legen Sie den Text fest, der den Benutzer auffordert, mit der rechten Maustaste auf dieses Feld zu klicken, um einen AutoText-Baustein auszuwählen.
    // dessen Inhalt das Feld anzeigen wird.
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
