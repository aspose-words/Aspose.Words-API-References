---
title: FindReplaceOptions.SmartParagraphBreakReplacement
second_title: Aspose.Words für .NET-API-Referenz
description: FindReplaceOptions eigendom. Ruft einen booleschen Wert ab oder legt ihn fest der angibt ob der Absatz break ersetzt werden darf wenn kein nächster gleichgeordneter Absatz vorhanden ist.
type: docs
weight: 160
url: /de/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob der Absatz break ersetzt werden darf, wenn kein nächster gleichgeordneter Absatz vorhanden ist.

Der Standardwert ist`FALSCH`.

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

### Bemerkungen

Diese Option ermöglicht das Ersetzen eines Absatzumbruchs, wenn es keinen nächsten gleichgeordneten Absatz gibt, in den alle untergeordneten Knoten verschoben werden können, indem nach dem zu ersetzenden Absatz ein beliebiger (nicht unbedingt gleichgeordneter) nächster Absatz gesucht wird.

### Beispiele

Zeigt, wie man einen Absatz aus einer Tabellenzelle mit einer verschachtelten Tabelle entfernt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Tabelle mit Absatz und innerer Tabelle in der ersten Zelle erstellen.
builder.StartTable();
builder.InsertCell();
builder.Write("TEXT1");
builder.StartTable();
builder.InsertCell();
builder.EndTable();
builder.EndTable();
builder.Writeln();

FindReplaceOptions options = new FindReplaceOptions();
// Wenn die folgende Option auf „true“ gesetzt ist, entfernt Aspose.Words den Text des Absatzes
// komplett mit seiner Absatzmarke. Andernfalls ahmt Aspose.Words Word nach und entfernt es
// nur den Text des Absatzes und lässt die Absatzmarke intakt (wenn eine Tabelle auf den Text folgt).
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../findreplaceoptions/)
* Montage [Aspose.Words](../../../)


