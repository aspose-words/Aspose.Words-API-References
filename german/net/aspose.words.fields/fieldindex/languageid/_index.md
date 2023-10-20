---
title: FieldIndex.LanguageId
linktitle: LanguageId
articleTitle: LanguageId
second_title: Aspose.Words für .NET
description: FieldIndex LanguageId eigendom. Ruft die SprachID ab die zum Generieren des Index verwendet wird oder legt diese fest in C#.
type: docs
weight: 80
url: /de/net/aspose.words.fields/fieldindex/languageid/
---
## FieldIndex.LanguageId property

Ruft die Sprach-ID ab, die zum Generieren des Index verwendet wird, oder legt diese fest.

```csharp
public string LanguageId { get; set; }
```

## Beispiele

Zeigt, wie man ein INDEX-Feld mithilfe von XE-Feldern mit Einträgen füllt und auch sein Erscheinungsbild ändert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das einen Eintrag für jedes im Dokument gefundene XE-Feld anzeigt.
// Jeder Eintrag zeigt den Text-Eigenschaftswert des XE-Felds auf der linken Seite an.
// und die Nummer der Seite, die rechts das XE-Feld enthält.
// Wenn die XE-Felder in ihrer Eigenschaft „Text“ den gleichen Wert haben,
// Das INDEX-Feld gruppiert sie in einem Eintrag.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);
index.LanguageId = "1033";

// Wenn Sie den Wert dieser Eigenschaft auf „A“ setzen, werden alle Einträge nach ihrem Anfangsbuchstaben gruppiert.
// und platzieren Sie diesen Buchstaben in Großbuchstaben über jeder Gruppe.
index.Heading = "A";

// Stellen Sie die durch das INDEX-Feld erstellte Tabelle so ein, dass sie sich über 2 Spalten erstreckt.
index.NumberOfColumns = "2";

// Alle Einträge mit Anfangsbuchstaben außerhalb des „ac“-Zeichenbereichs so festlegen, dass sie weggelassen werden.
index.LetterRange = "a-c";

Assert.AreEqual(" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index.GetFieldCode());

// Diese nächsten beiden XE-Felder werden unter der Überschrift „A“ angezeigt.
// mit ihren jeweiligen Textstilen, die auch auf ihre Seitenzahlen angewendet werden.
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

// Die beiden nächsten XE-Felder stehen im Inhaltsverzeichnis der INDEX-Felder unter der Überschrift „B“ und „C“.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Banana";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cherry";

// INDEX-Felder sortieren alle Einträge alphabetisch, sodass dieser Eintrag zusammen mit den anderen beiden unter „A“ angezeigt wird.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Avocado";

// Dieser Eintrag wird nicht angezeigt, da er mit dem Buchstaben „D“ beginnt.
// was außerhalb des „ac“-Zeichenbereichs liegt, den die LetterRange-Eigenschaft des INDEX-Felds definiert.
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
