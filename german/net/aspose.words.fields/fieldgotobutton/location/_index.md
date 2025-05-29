---
title: FieldGoToButton.Location
linktitle: Location
articleTitle: Location
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldGoToButton-Standorteigenschaft und legen Sie ganz einfach Lesezeichen, Seitenzahlen oder Elemente für eine nahtlose Navigation und ein verbessertes Benutzererlebnis fest.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldgotobutton/location/
---
## FieldGoToButton.Location property

Ruft den Namen eines Lesezeichens, eine Seitenzahl oder ein anderes Element ab, zu dem gesprungen werden soll, oder legt diesen fest.

```csharp
public string Location { get; set; }
```

## Beispiele

Zeigt, wie ein GOTOBUTTON-Feld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein GOTOBUTTON-Feld hinzu. Wenn wir in Microsoft Word auf dieses Feld doppelklicken,
// Dadurch wird der Textcursor zum Lesezeichen bewegt, auf dessen Namen die Eigenschaft „Location“ verweist.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// Fügen Sie ein gültiges Lesezeichen für das zu referenzierende Feld ein.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark(field.Location);
builder.Writeln("Bookmark text contents.");
builder.EndBookmark(field.Location);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.GOTOBUTTON.docx");
```

### Siehe auch

* class [FieldGoToButton](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
