---
title: FieldGoToButton.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: Aspose.Words für .NET
description: Passen Sie die DisplayText-Eigenschaft Ihres FieldGoToButton an, um die Benutzerfreundlichkeit zu verbessern. Legen Sie einfach den Schaltflächentext für eine nahtlose Dokumentennavigation und schnellen Zugriff fest.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldgotobutton/displaytext/
---
## FieldGoToButton.DisplayText property

Ruft den Text der „Schaltfläche“ ab oder legt ihn fest, der im Dokument angezeigt wird, sodass er zum Aktivieren des Sprungs ausgewählt werden kann.

```csharp
public string DisplayText { get; set; }
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
