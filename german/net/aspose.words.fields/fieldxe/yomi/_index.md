---
title: FieldXE.Yomi
linktitle: Yomi
articleTitle: Yomi
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Indexeinträge mit der FieldXE Yomi-Eigenschaft und ermöglichen Sie eine effiziente Sortierung mithilfe des ersten phonetischen Zeichens für eine verbesserte Datenorganisation.
type: docs
weight: 80
url: /de/net/aspose.words.fields/fieldxe/yomi/
---
## FieldXE.Yomi property

Ruft das Yomi (erstes phonetisches Zeichen zum Sortieren von Indizes) für den Indexeintrag ab oder legt es fest

```csharp
public string Yomi { get; set; }
```

## Beispiele

Zeigt, wie INDEX-Feldeinträge phonetisch sortiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein INDEX-Feld, das für jedes im Dokument gefundene XE-Feld einen Eintrag anzeigt.
// Jeder Eintrag zeigt auf der linken Seite den Text-Eigenschaftswert des XE-Felds an,
// und die Nummer der Seite, die rechts das XE-Feld enthält.
// Der INDEX-Eintrag sammelt alle XE-Felder mit übereinstimmenden Werten in der Eigenschaft "Text"
// in einen Eintrag, anstatt für jedes XE-Feld einen Eintrag zu erstellen.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Die INDEX-Tabelle sortiert ihre Einträge automatisch nach den Werten ihrer Texteigenschaften in alphabetischer Reihenfolge.
// Legen Sie die INDEX-Tabelle so fest, dass die Einträge stattdessen phonetisch mit Hiragana sortiert werden.
index.UseYomi = sortEntriesUsingYomi;

if (sortEntriesUsingYomi)
    Assert.AreEqual(" INDEX  \\y", index.GetFieldCode());
else
    Assert.AreEqual(" INDEX ", index.GetFieldCode());

// Fügen Sie 4 XE-Felder ein, die als Einträge im Inhaltsverzeichnis des INDEX-Felds angezeigt werden.
// Die Eigenschaft "Text" kann die Schreibweise eines Wortes in Kanji enthalten, dessen Aussprache mehrdeutig sein kann,
// während die „Yomi“-Version des Wortes genau so geschrieben wird, wie es in Hiragana ausgesprochen wird.
// Wenn wir unser INDEX-Feld so einstellen, dass es Yomi verwendet, werden diese Einträge sortiert
// durch den Wert ihrer Yomi-Eigenschaften, statt durch ihre Textwerte.
builder.InsertBreak(BreakType.PageBreak);
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛子";
indexEntry.Yomi = "あ";

Assert.AreEqual(" XE  愛子 \\y あ", indexEntry.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "明美";
indexEntry.Yomi = "あ";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "恵美";
indexEntry.Yomi = "え";

builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "愛美";
indexEntry.Yomi = "え";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Yomi.docx");
```

### Siehe auch

* class [FieldXE](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
