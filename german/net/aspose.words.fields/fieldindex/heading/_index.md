---
title: FieldIndex.Heading
linktitle: Heading
articleTitle: Heading
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldIndex-Überschrifteneigenschaft, um Eintragsüberschriften nach Buchstaben anzupassen und so die Organisation und Benutzererfahrung in Ihrer Anwendung zu verbessern.
type: docs
weight: 70
url: /de/net/aspose.words.fields/fieldindex/heading/
---
## FieldIndex.Heading property

Ruft eine Überschrift ab oder legt sie fest, die am Anfang jedes Eintragssatzes für einen beliebigen Buchstaben angezeigt wird.

```csharp
public string Heading { get; set; }
```

## Beispiele

Zeigt, wie Sie ein INDEX-Feld mithilfe von XE-Feldern mit Einträgen füllen und auch sein Erscheinungsbild ändern.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt auf der linken Seite den Text-Eigenschaftswert des XE-Felds an,
// und die Nummer der Seite, die rechts das XE-Feld enthält.
// Wenn die XE-Felder den gleichen Wert in ihrer Eigenschaft "Text" haben,
// Das INDEX-Feld gruppiert sie in einem Eintrag.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Wenn Sie den Wert dieser Eigenschaft auf „A“ setzen, werden alle Einträge nach ihrem Anfangsbuchstaben gruppiert.
// und platzieren Sie diesen Buchstaben als Großbuchstaben über jeder Gruppe.
index.Heading = "A";

// Legen Sie fest, dass die durch das INDEX-Feld erstellte Tabelle sich über zwei Spalten erstreckt.
index.NumberOfColumns = "2";

// Legen Sie fest, dass alle Einträge mit Anfangsbuchstaben außerhalb des Zeichenbereichs „ac“ weggelassen werden.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Die nächsten beiden XE-Felder werden unter der Überschrift „A“ angezeigt.
// mit den jeweiligen Textformatierungen, die auch auf die Seitenzahlen angewendet werden.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apple";
indexEntry.IsItalic = true;

Assert.AreEqual(" XE  Apple \\i", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Apricot";
indexEntry.IsBold = true;

Assert.AreEqual(" XE  Apricot \\b", indexEntry.GetFieldCode());

// Die nächsten beiden XE-Felder stehen im Inhaltsverzeichnis der INDEX-Felder unter der Überschrift „B“ und „C“.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// INDEX-Felder sortieren alle Einträge alphabetisch, sodass dieser Eintrag mit den anderen beiden unter „A“ angezeigt wird.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Dieser Eintrag wird nicht angezeigt, da er mit dem Buchstaben "D" beginnt,
// der außerhalb des „ac“-Zeichenbereichs liegt, der durch die LetterRange-Eigenschaft des INDEX-Felds definiert wird.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Durian";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Formatting.docx");
```

### Siehe auch

* class [FieldIndex](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
