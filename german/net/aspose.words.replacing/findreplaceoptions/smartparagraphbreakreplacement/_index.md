---
title: FindReplaceOptions.SmartParagraphBreakReplacement
linktitle: SmartParagraphBreakReplacement
articleTitle: SmartParagraphBreakReplacement
second_title: Aspose.Words für .NET
description: Entdecken Sie die SmartParagraphBreakReplacement-Eigenschaft in FindReplaceOptions. Steuern Sie Absatzumbrüche mühelos für eine nahtlose Textformatierung.
type: docs
weight: 170
url: /de/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

Ruft einen Booleschen Wert ab oder legt ihn fest, der angibt, ob der Absatz „break “ ersetzt werden darf, wenn kein nächster gleichgeordneter Absatz vorhanden ist.

Der Standardwert ist`FALSCH`.

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

## Bemerkungen

Mit dieser Option können Sie einen Absatzumbruch ersetzen, wenn kein nächster gleichgeordneter Absatz vorhanden ist, zu dem alle untergeordneten Knoten verschoben werden können. Dazu wird ein beliebiger (nicht unbedingt gleichgeordneter) nächster Absatz nach dem zu ersetzenden Absatz gesucht.

## Beispiele

Zeigt, wie Sie mit einer verschachtelten Tabelle einen Absatz aus einer Tabellenzelle entfernen.

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
// vollständig mit Absatzmarke. Andernfalls ahmt Aspose.Words Word nach und entfernt
// nur Absatztext und lässt die Absatzmarke intakt (wenn auf den Text eine Tabelle folgt).
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### Siehe auch

* class [FindReplaceOptions](../)
* namensraum [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Montage [Aspose.Words](../../../)
