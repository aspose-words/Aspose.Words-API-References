---
title: FieldGoToButton.Location
linktitle: Location
articleTitle: Location
second_title: Aspose.Words für .NET
description: FieldGoToButton Location eigendom. Ruft den Namen eines Lesezeichens eine Seitenzahl oder ein anderes Element ab zu dem gesprungen werden soll oder legt diesen fest in C#.
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

Zeigt an, dass ein GOTOBUTTON-Feld eingefügt werden soll.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein GOTOBUTTON-Feld hinzufügen. Wenn wir in Microsoft Word auf dieses Feld doppelklicken,
// Der Textcursor wird zum Lesezeichen geführt, auf dessen Namen die Location-Eigenschaft verweist.
FieldGoToButton field = (FieldGoToButton)builder.InsertField(FieldType.FieldGoToButton, true);
field.DisplayText = "My Button";
field.Location = "MyBookmark";

Assert.AreEqual(" GOTOBUTTON  MyBookmark My Button", field.GetFieldCode());

// Ein gültiges Lesezeichen für das Feld einfügen, auf das verwiesen werden soll.
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
