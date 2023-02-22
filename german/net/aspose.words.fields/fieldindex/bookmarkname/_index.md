---
title: FieldIndex.BookmarkName
second_title: Aspose.Words für .NET-API-Referenz
description: FieldIndex eigendom. Ruft den Namen des Lesezeichens ab oder legt ihn fest das den Teil des Dokuments markiert der zum Erstellen des Index verwendet wurde.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldindex/bookmarkname/
---
## FieldIndex.BookmarkName property

Ruft den Namen des Lesezeichens ab oder legt ihn fest, das den Teil des Dokuments markiert, der zum Erstellen des Index verwendet wurde.

```csharp
public string BookmarkName { get; set; }
```

### Beispiele

Zeigt, wie Sie ein INDEX-Feld erstellen und es dann mithilfe von XE-Feldern mit Einträgen füllen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das einen Eintrag für jedes im Dokument gefundene XE-Feld anzeigt.
// Jeder Eintrag zeigt den Text-Eigenschaftswert des XE-Felds auf der linken Seite an
// und rechts die Seite mit dem XE-Feld.
// Wenn die XE-Felder den gleichen Wert in ihrer "Text"-Eigenschaft haben,
// das Feld INDEX gruppiert sie zu einem Eintrag.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Konfigurieren Sie das INDEX-Feld nur so, dass XE-Felder angezeigt werden, die innerhalb der Grenzen liegen
// eines Lesezeichens mit dem Namen "MainBookmark" und dessen "EntryType"-Eigenschaften den Wert "A" haben.
// Sowohl für INDEX- als auch für XE-Felder verwendet die Eigenschaft "EntryType" nur das erste Zeichen ihres Zeichenfolgenwerts.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// Beginnen Sie auf einer neuen Seite das Lesezeichen mit einem Namen, der dem Wert entspricht
// der Eigenschaft "BookmarkName" des INDEX-Felds.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// Das INDEX-Feld nimmt diesen Eintrag auf, da er sich innerhalb des Lesezeichens befindet,
// und sein Eintragstyp stimmt auch mit dem Eintragstyp des INDEX-Felds überein.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Fügen Sie ein XE-Feld ein, das nicht im INDEX erscheint, da die Eintragstypen nicht übereinstimmen.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Lesezeichen beenden und danach ein XE-Feld einfügen.
// Es ist vom gleichen Typ wie das INDEX-Feld, wird aber nicht angezeigt
// da es außerhalb der Grenzen des Lesezeichens liegt.
builder.EndBookmark("MainBookmark");
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 3";
indexEntry.EntryType = "A";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Filtering.docx");
```

### Siehe auch

* class [FieldIndex](../)
* namensraum [Aspose.Words.Fields](../../fieldindex/)
* Montage [Aspose.Words](../../../)


