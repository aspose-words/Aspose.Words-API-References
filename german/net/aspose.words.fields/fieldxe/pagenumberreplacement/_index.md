---
title: FieldXE.PageNumberReplacement
linktitle: PageNumberReplacement
articleTitle: PageNumberReplacement
second_title: Aspose.Words für .NET
description: FieldXE PageNumberReplacement eigendom. Ruft Text ab der anstelle einer Seitenzahl verwendet wird oder legt diesen fest in C#.
type: docs
weight: 50
url: /de/net/aspose.words.fields/fieldxe/pagenumberreplacement/
---
## FieldXE.PageNumberReplacement property

Ruft Text ab, der anstelle einer Seitenzahl verwendet wird, oder legt diesen fest.

```csharp
public string PageNumberReplacement { get; set; }
```

## Beispiele

Zeigt, wie Querverweise in einem INDEX-Feld definiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das einen Eintrag für jedes im Dokument gefundene XE-Feld anzeigt.
// Jeder Eintrag zeigt den Text-Eigenschaftswert des XE-Felds auf der linken Seite an.
// und die Nummer der Seite, die rechts das XE-Feld enthält.
// Der INDEX-Eintrag sammelt alle XE-Felder mit übereinstimmenden Werten in der Eigenschaft „Text“.
// in einen Eintrag, anstatt für jedes XE-Feld einen Eintrag vorzunehmen.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Wir können ein XE-Feld so konfigurieren, dass sein INDEX-Eintrag eine Zeichenfolge anstelle einer Seitenzahl anzeigt.
// Erstens, für Einträge, die eine Seitenzahl durch eine Zeichenfolge ersetzen,
// Geben Sie ein benutzerdefiniertes Trennzeichen zwischen dem Text-Eigenschaftswert des XE-Felds und der Zeichenfolge an.
index.CrossReferenceSeparator = ", see: ";

Assert.AreEqual(" INDEX  \\k \", see: \"", index.GetFieldCode());

// Ein XE-Feld einfügen, das einen regulären INDEX-Eintrag erstellt, der die Seitenzahl dieses Feldes anzeigt,
// und ruft den CrossReferenceSeparator-Wert nicht auf.
// Der Eintrag für dieses XE-Feld zeigt „Apple, 2“ an.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";

Assert.AreEqual(" XE  Apple", indexEntry.GetFieldCode());

// Ein weiteres XE-Feld auf Seite 3 einfügen und einen Wert für die PageNumberReplacement-Eigenschaft festlegen.
// Dieser Wert wird anstelle der Nummer der Seite angezeigt, auf der sich dieses Feld befindet.
// und der CrossReferenceSeparator-Wert des INDEX-Feldes wird davor angezeigt.
// Der Eintrag für dieses XE-Feld zeigt „Banane, siehe: Tropische Früchte“.
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

* class [FieldXE](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
