---
title: FieldXE.EntryType
linktitle: EntryType
articleTitle: EntryType
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldXE EntryType-Eigenschaft, verwalten und passen Sie Indexeintragstypen einfach an, um die Datenorganisation und Abrufeffizienz zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldxe/entrytype/
---
## FieldXE.EntryType property

Ruft einen Indexeintragstyp ab oder legt ihn fest.

```csharp
public string EntryType { get; set; }
```

## Beispiele

Zeigt, wie Sie ein INDEX-Feld erstellen und es dann mithilfe von XE-Feldern mit Einträgen füllen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt den Text-Eigenschaftswert des XE-Felds auf der linken Seite an
// und die Seite mit dem XE-Feld auf der rechten Seite.
// Wenn die XE-Felder den gleichen Wert in ihrer Eigenschaft "Text" haben,
// Das INDEX-Feld gruppiert sie in einem Eintrag.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Konfigurieren Sie das INDEX-Feld nur so, dass XE-Felder angezeigt werden, die innerhalb der Grenzen liegen
// eines Lesezeichens mit dem Namen „MainBookmark“, dessen „EntryType“-Eigenschaften den Wert „A“ haben.
// Sowohl für INDEX- als auch für XE-Felder verwendet die Eigenschaft „EntryType“ nur das erste Zeichen ihres Zeichenfolgenwerts.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// Beginnen Sie das Lesezeichen auf einer neuen Seite mit einem Namen, der dem Wert entspricht
// der Eigenschaft „BookmarkName“ des INDEX-Felds.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// Das INDEX-Feld wird diesen Eintrag aufnehmen, da er sich innerhalb des Lesezeichens befindet.
// und sein Eintragstyp entspricht auch dem Eintragstyp des INDEX-Felds.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Fügen Sie ein XE-Feld ein, das nicht im INDEX angezeigt wird, da die Eintragstypen nicht übereinstimmen.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Beenden Sie das Lesezeichen und fügen Sie anschließend ein XE-Feld ein.
// Es ist vom gleichen Typ wie das INDEX-Feld, wird aber nicht angezeigt
// da es außerhalb der Grenzen des Lesezeichens liegt.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

### Siehe auch

* class [FieldXE](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
