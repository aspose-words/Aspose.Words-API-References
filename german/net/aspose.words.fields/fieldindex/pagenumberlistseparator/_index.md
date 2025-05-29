---
title: FieldIndex.PageNumberListSeparator
linktitle: PageNumberListSeparator
articleTitle: PageNumberListSeparator
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldIndex-Eigenschaft PageNumberListSeparator, um die Seitenzahlenformatierung mühelos anzupassen. Verbessern Sie noch heute die Lesbarkeit Ihres Dokuments!
type: docs
weight: 110
url: /de/net/aspose.words.fields/fieldindex/pagenumberlistseparator/
---
## FieldIndex.PageNumberListSeparator property

Ruft die Zeichenfolge ab oder legt sie fest, die zum Trennen zweier Seitenzahlen in einer Seitenzahlenliste verwendet wird.

```csharp
public string PageNumberListSeparator { get; set; }
```

## Beispiele

Zeigt, wie das Seitenzahlentrennzeichen in einem INDEX-Feld bearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt auf der linken Seite den Text-Eigenschaftswert des XE-Felds an,
// und die Nummer der Seite, die rechts das XE-Feld enthält.
// Der INDEX-Eintrag gruppiert XE-Felder mit übereinstimmenden Werten in der Eigenschaft "Text"
// in einen Eintrag, anstatt für jedes XE-Feld einen Eintrag zu erstellen.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Wenn unser INDEX-Feld einen Eintrag für eine Gruppe von XE-Feldern hat,
// Dieser Eintrag zeigt die Nummer jeder Seite an, die ein XE-Feld enthält, das zu dieser Gruppe gehört.
// Wir können benutzerdefinierte Trennzeichen festlegen, um das Erscheinungsbild dieser Seitenzahlen anzupassen.
index.PageNumberSeparator = ", on page(s) ";
index.PageNumberListSeparator = " & ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\l \" & \"", index.GetFieldCode());
Assert.True(index.HasPageNumberSeparator);

// Nachdem wir diese XE-Felder eingefügt haben, zeigt das INDEX-Feld „Erster Eintrag auf Seite(n) 2 & 3 & 4“ an.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

Assert.AreEqual(" XE  \"First entry\"", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "First entry";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageNumberList.docx");
```

### Siehe auch

* class [FieldIndex](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
