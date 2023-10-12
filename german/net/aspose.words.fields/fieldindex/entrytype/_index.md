---
title: FieldIndex.EntryType
second_title: Aspose.Words für .NET-API-Referenz
description: FieldIndex eigendom. Ruft einen Indexeintragstyp ab der zum Erstellen des Index verwendet wird oder legt diesen fest.
type: docs
weight: 40
url: /de/net/aspose.words.fields/fieldindex/entrytype/
---
## FieldIndex.EntryType property

Ruft einen Indexeintragstyp ab, der zum Erstellen des Index verwendet wird, oder legt diesen fest.

```csharp
public string EntryType { get; set; }
```

### Beispiele

Zeigt, wie Sie ein INDEX-Feld erstellen und es dann mithilfe von XE-Feldern mit Einträgen füllen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das einen Eintrag für jedes im Dokument gefundene XE-Feld anzeigt.
// Bei jedem Eintrag wird der Text-Eigenschaftswert des XE-Felds auf der linken Seite angezeigt
// und die Seite mit dem XE-Feld rechts.
// Wenn die XE-Felder in ihrer Eigenschaft „Text“ den gleichen Wert haben,
// Das INDEX-Feld gruppiert sie in einem Eintrag.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Konfigurieren Sie das INDEX-Feld nur so, dass XE-Felder angezeigt werden, die innerhalb der Grenzen liegen
// eines Lesezeichens mit dem Namen „MainBookmark“, dessen „EntryType“-Eigenschaften den Wert „A“ haben.
// Sowohl für INDEX- als auch für XE-Felder verwendet die Eigenschaft „EntryType“ nur das erste Zeichen ihres Zeichenfolgewerts.
index.BookmarkName = "MainBookmark";
index.EntryType = "A";

Assert.AreEqual(" INDEX  \\b MainBookmark \\f A", index.GetFieldCode());

// Beginnen Sie auf einer neuen Seite das Lesezeichen mit einem Namen, der dem Wert entspricht
// der Eigenschaft „BookmarkName“ des INDEX-Felds.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MainBookmark");

// Das INDEX-Feld übernimmt diesen Eintrag, da er sich im Lesezeichen befindet.
// und sein Eintragstyp stimmt auch mit dem Eintragstyp des INDEX-Felds überein.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 1";
indexEntry.EntryType = "A";

Assert.AreEqual(" XE  \"Index entry 1\" \\f A", indexEntry.GetFieldCode());

// Ein XE-Feld einfügen, das nicht im INDEX erscheint, weil die Eintragstypen nicht übereinstimmen.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Index entry 2";
indexEntry.EntryType = "B";

// Lesezeichen beenden und anschließend ein XE-Feld einfügen.
// Es ist vom gleichen Typ wie das INDEX-Feld, wird aber nicht angezeigt
// da es außerhalb der Lesezeichengrenzen liegt.
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

* class [FieldIndex](../)
* namensraum [Aspose.Words.Fields](../../fieldindex/)
* Montage [Aspose.Words](../../../)


