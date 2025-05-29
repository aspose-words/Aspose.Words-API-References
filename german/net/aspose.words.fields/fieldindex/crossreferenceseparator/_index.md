---
title: FieldIndex.CrossReferenceSeparator
linktitle: CrossReferenceSeparator
articleTitle: CrossReferenceSeparator
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldIndex CrossReferenceSeparator-Eigenschaft, um Zeichenfolgen zum effizienten Trennen von Querverweisen und Einträgen einfach zu verwalten.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldindex/crossreferenceseparator/
---
## FieldIndex.CrossReferenceSeparator property

Ruft die Zeichenfolge ab oder legt sie fest, die zum Trennen von Querverweisen und anderen Einträgen verwendet wird.

```csharp
public string CrossReferenceSeparator { get; set; }
```

## Beispiele

Zeigt, wie Querverweise in einem INDEX-Feld definiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt auf der linken Seite den Text-Eigenschaftswert des XE-Felds an,
// und die Nummer der Seite, die rechts das XE-Feld enthält.
// Der INDEX-Eintrag sammelt alle XE-Felder mit übereinstimmenden Werten in der Eigenschaft "Text"
// in einen Eintrag, anstatt für jedes XE-Feld einen Eintrag zu erstellen.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Wir können ein XE-Feld so konfigurieren, dass in seinem INDEX-Eintrag eine Zeichenfolge statt einer Seitenzahl angezeigt wird.
// Erstens, für Einträge, die eine Seitenzahl durch eine Zeichenfolge ersetzen,
// Geben Sie ein benutzerdefiniertes Trennzeichen zwischen dem Texteigenschaftswert des XE-Felds und der Zeichenfolge an.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// Fügt ein XE-Feld ein, das einen regulären INDEX-Eintrag erstellt, der die Seitenzahl dieses Feldes anzeigt,
// und ruft den CrossReferenceSeparator-Wert nicht auf.
// Der Eintrag für dieses XE-Feld zeigt „Apple, 2“ an.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// Fügen Sie auf Seite 3 ein weiteres XE-Feld ein und legen Sie einen Wert für die Eigenschaft PageNumberReplacement fest.
// Dieser Wert wird anstelle der Nummer der Seite angezeigt, auf der sich dieses Feld befindet.
// und der CrossReferenceSeparator-Wert des INDEX-Felds wird davor angezeigt.
// Der Eintrag für dieses XE-Feld zeigt „Banane, siehe: Tropische Frucht“ an.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";
indexEntry.PageNumberReplacement = "Tropical fruit";

Assert.AreEqual(" XE  Banana \\t \"Tropical fruit\"", indexEntry.GetFieldCode());

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.CrossReferenceSeparator.docx");
```

### Siehe auch

* class [FieldIndex](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
