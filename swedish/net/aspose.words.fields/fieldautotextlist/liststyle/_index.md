---
title: FieldAutoTextList.ListStyle
linktitle: ListStyle
articleTitle: ListStyle
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldAutoTextList ListStyle för att enkelt anpassa dina postlistor. Förbättra ditt innehåll med skräddarsydda stilar idag!
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldautotextlist/liststyle/
---
## FieldAutoTextList.ListStyle property

Hämtar eller anger namnet på den stil som listan som ska innehålla poster baseras på.

```csharp
public string ListStyle { get; set; }
```

## Exempel

Visar hur man använder ett AUTOTEXTLIST-fält för att välja från en lista med AutoText-poster.

```csharp
public void FieldAutoTextList()
{
    Document doc = new Document();

    // Skapa ett ordlistadokument och fyll det med automatiska textinmatningar.
    doc.GlossaryDocument = new GlossaryDocument();
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 1", "Contents of AutoText 1");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 2", "Contents of AutoText 2");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 3", "Contents of AutoText 3");

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Skapa ett AUTOTEXTLIST-fält och ange texten som fältet ska visa i Microsoft Word.
    // Ställ in texten så att användaren högerklickar på det här fältet för att välja ett AutoText-byggblock,
    // vars innehåll fältet kommer att visa.
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
/// Skapa ett byggblock av AutoText-typ och lägg till det i ett ordlistadokument.
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

### Se även

* class [FieldAutoTextList](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
