---
title: DocumentBase.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words für .NET
description: Importieren Sie mühelos Knoten aus anderen Dokumenten und optimieren Sie Ihren Workflow mit der ImportNode-Methode von DocumentBase. Optimieren Sie Ihr Dokumentenmanagement noch heute!
type: docs
weight: 110
url: /de/net/aspose.words/documentbase/importnode/
---
## ImportNode(*[Node](../../node/), bool*) {#importnode}

Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcNode | Node | Der Knoten, der importiert wird. |
| isImportChildren | Boolean | `WAHR` um alle untergeordneten Knoten rekursiv zu importieren; andernfalls`FALSCH`. |

### Rückgabewert

Der geklonte Knoten, der zum aktuellen Dokument gehört.

## Bemerkungen

Diese Methode verwendet dieUseDestinationStyles Option zum Auflösen der Formatierung.

Beim Importieren eines Knotens wird eine Kopie des Quellknotens des importierenden Dokuments erstellt. Der zurückgegebene Knoten hat keinen übergeordneten Knoten. Der Quellknoten wird weder geändert noch aus dem Originaldokument entfernt.

Bevor ein Knoten aus einem anderen Dokument in dieses eingefügt werden kann, muss er importiert werden. Beim Import werden dokumentspezifische Eigenschaften wie Referenzen auf Stile und Listen vom Originaldokument in das importierende Dokument übertragen. Nach dem Import kann der Knoten an der entsprechenden Stelle im Dokument eingefügt werden.[`InsertBefore`](../../compositenode/insertbefore/) oder [`InsertAfter`](../../compositenode/insertafter/).

Wenn der Quellknoten bereits zum Zieldokument gehört, wird einfach ein tiefer Klon des Quellknotens erstellt.

## Beispiele

Zeigt, wie ein Knoten von einem Dokument in ein anderes importiert wird.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// Jeder Knoten hat ein übergeordnetes Dokument, das den Knoten enthält.
// Das Einfügen eines Knotens in ein Dokument, zu dem der Knoten nicht gehört, löst eine Ausnahme aus.
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => dstDoc.AppendChild(srcDoc.FirstSection));

// Verwenden Sie die ImportNode-Methode, um eine Kopie eines Knotens zu erstellen, der das Dokument enthält
// das die ImportNode-Methode aufgerufen hat, die als neues Besitzerdokument festgelegt wurde.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true);

Assert.AreEqual(dstDoc, importedSection.Document);

// Wir können jetzt den Knoten in das Dokument einfügen.
dstDoc.AppendChild(importedSection);

Assert.AreEqual("Destination document first paragraph text.\r\nSource document first paragraph text.\r\n",
    dstDoc.ToString(SaveFormat.Text));
```

### Siehe auch

* class [Node](../../node/)
* class [DocumentBase](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## ImportNode(*[Node](../../node/), bool, [ImportFormatMode](../../importformatmode/)*) {#importnode_1}

Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument mit einer Option zur Steuerung der Formatierung.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren, ImportFormatMode importFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcNode | Node | Der zu importierende Knoten. |
| isImportChildren | Boolean | `WAHR` um alle untergeordneten Knoten rekursiv zu importieren; andernfalls`FALSCH`. |
| importFormatMode | ImportFormatMode | Gibt an, wie kollidierende Stilformatierungen zusammengeführt werden. |

### Rückgabewert

Der geklonte, importierte Knoten. Der Knoten gehört zum Zieldokument, hat aber kein übergeordnetes Dokument.

## Bemerkungen

Diese Überladung ist nützlich, um zu steuern, wie Stile und Listenformatierungen importiert werden.

Beim Importieren eines Knotens wird eine Kopie des Quellknotens des importierenden Dokuments erstellt. Der zurückgegebene Knoten hat keinen übergeordneten Knoten. Der Quellknoten wird weder geändert noch aus dem Originaldokument entfernt.

Bevor ein Knoten aus einem anderen Dokument in dieses eingefügt werden kann, muss er importiert werden. Beim Import werden dokumentspezifische Eigenschaften wie Referenzen auf Stile und Listen vom Originaldokument in das importierende Dokument übertragen. Nach dem Import kann der Knoten an der entsprechenden Stelle im Dokument eingefügt werden.[`InsertBefore`](../../compositenode/insertbefore/) oder [`InsertAfter`](../../compositenode/insertafter/).

Wenn der Quellknoten bereits zum Zieldokument gehört, wird einfach ein tiefer Klon des Quellknotens erstellt.

## Beispiele

Zeigt, wie Knoten mit bestimmten Optionen vom Quelldokument in das Zieldokument importiert werden.

```csharp
// Erstellen Sie zwei Dokumente und fügen Sie jedem Dokument einen Zeichenstil hinzu.
// Konfigurieren Sie die Stile so, dass sie denselben Namen, aber unterschiedliche Textformatierungen haben.
Document srcDoc = new Document();
Style srcStyle = srcDoc.Styles.Add(StyleType.Character, "My style");
srcStyle.Font.Name = "Courier New";
DocumentBuilder srcBuilder = new DocumentBuilder(srcDoc);
srcBuilder.Font.Style = srcStyle;
srcBuilder.Writeln("Source document text.");

Document dstDoc = new Document();
Style dstStyle = dstDoc.Styles.Add(StyleType.Character, "My style");
dstStyle.Font.Name = "Calibri";
DocumentBuilder dstBuilder = new DocumentBuilder(dstDoc);
dstBuilder.Font.Style = dstStyle;
dstBuilder.Writeln("Destination document text.");

// Importieren Sie den Abschnitt aus dem Zieldokument in das Quelldokument, was zu einer Stilnamenkollision führt.
// Wenn wir Zielstile verwenden, dann wird der importierte Quelltext mit dem gleichen Stilnamen
// da der Zieltext den Zielstil übernimmt.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// Wenn wir ImportFormatMode.KeepDifferentStyles verwenden, bleibt der Quellstil erhalten,
// und der Namenskonflikt wird durch Hinzufügen eines Suffixes gelöst.
dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.KeepDifferentStyles);
Assert.AreEqual(dstStyle.Font.Name, dstDoc.Styles["My style"].Font.Name);
Assert.AreEqual(srcStyle.Font.Name, dstDoc.Styles["My style_0"].Font.Name);
```

### Siehe auch

* class [Node](../../node/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBase](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
