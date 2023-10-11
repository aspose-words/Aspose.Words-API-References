---
title: FieldGoToButton.DisplayText
second_title: Aspose.Words für .NET-API-Referenz
description: FieldGoToButton eigendom. Ruft den Text der Schaltfläche ab die im Dokument angezeigt wird oder legt diesen fest sodass er zum Aktivieren des Sprungs ausgewählt werden kann.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldgotobutton/displaytext/
---
## FieldGoToButton.DisplayText property

Ruft den Text der „Schaltfläche“ ab, die im Dokument angezeigt wird, oder legt diesen fest, sodass er zum Aktivieren des Sprungs ausgewählt werden kann.

```csharp
public string DisplayText { get; set; }
```

### Beispiele

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
* namensraum [Aspose.Words.Fields](../../fieldgotobutton/)
* Montage [Aspose.Words](../../../)


