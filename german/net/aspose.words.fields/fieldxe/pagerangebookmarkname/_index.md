---
title: FieldXE.PageRangeBookmarkName
linktitle: PageRangeBookmarkName
articleTitle: PageRangeBookmarkName
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldXE-Eigenschaft PageRangeBookmarkName – verwalten Sie Lesezeichennamen effizient für eine präzise Seitenbereichsverfolgung in Ihren Dokumenten.
type: docs
weight: 60
url: /de/net/aspose.words.fields/fieldxe/pagerangebookmarkname/
---
## FieldXE.PageRangeBookmarkName property

Ruft den Namen des Lesezeichens ab oder legt ihn fest, das einen Seitenbereich markiert, der als Seitenzahl des Eintrags eingefügt wird.

```csharp
public string PageRangeBookmarkName { get; set; }
```

## Beispiele

Zeigt, wie die Seiten eines Lesezeichens als Seitenbereich für einen INDEX-Feldeintrag angegeben werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt auf der linken Seite den Text-Eigenschaftswert des XE-Felds an,
// und die Nummer der Seite, die rechts das XE-Feld enthält.
// Der INDEX-Eintrag sammelt alle XE-Felder mit übereinstimmenden Werten in der Eigenschaft "Text"
// in einen Eintrag, anstatt für jedes XE-Feld einen Eintrag zu erstellen.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Für INDEX-Einträge, die Seitenbereiche anzeigen, können wir eine Trennzeichenfolge angeben
// die zwischen der Nummer der ersten Seite und der Nummer der letzten Seite erscheinen wird.
index.PageNumberSeparator = ", on page(s) ";
index.PageRangeSeparator = " to ";

Assert.AreEqual(" INDEX  \\e \", on page(s) \" \\g \" to \"", index.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "My entry";

// Wenn ein XE-Feld ein Lesezeichen mit der Eigenschaft PageRangeBookmarkName benennt,
// sein INDEX-Eintrag zeigt den Seitenbereich an, den das Lesezeichen umfasst
// anstelle der Nummer der Seite, die das XE-Feld enthält.
indexEntry.PageRangeBookmarkName = "MyBookmark";

Assert.AreEqual(" XE  \"My entry\" \\r MyBookmark", indexEntry.GetFieldCode());
Assert.AreEqual("MyBookmark", indexEntry.PageRangeBookmarkName);

// Fügt ein Lesezeichen ein, das auf Seite 3 beginnt und auf Seite 5 endet.
// Der INDEX-Eintrag für das XE-Feld, das auf dieses Lesezeichen verweist, zeigt diesen Seitenbereich an.
// In unserer Tabelle wird im INDEX-Eintrag „Mein Eintrag, auf Seite(n) 3 bis 5“ angezeigt.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("MyBookmark");
builder.Write("Start of MyBookmark");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);
builder.Write("End of MyBookmark");
builder.EndBookmark("MyBookmark");

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.PageRangeBookmark.docx");
```

### Siehe auch

* class [FieldXE](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
