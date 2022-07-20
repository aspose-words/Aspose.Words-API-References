---
title: ImportNode
second_title: Aspose.Words für .NET-API-Referenz
description: Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument.
type: docs
weight: 100
url: /de/net/aspose.words/documentbase/importnode/
---
## ImportNode(Node, bool) {#importnode}

Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcNode | Node | Der Knoten, der importiert wird. |
| isImportChildren | Boolean | True, um alle untergeordneten Knoten rekursiv zu importieren; andernfalls falsch. |

### Rückgabewert

Der geklonte Knoten, der zum aktuellen Dokument gehört.

### Bemerkungen

Diese Methode verwendet dieUseDestinationStyles Option zum Auflösen der Formatierung.

Beim Importieren eines Knotens wird eine Kopie des Quellknotens erstellt, der zum importierenden Dokument gehört. Der zurückgegebene Knoten hat keinen Elternknoten. Der Quellknoten wird nicht geändert oder aus dem Originaldokument entfernt.

Bevor ein Knoten aus einem anderen Dokument in dieses Dokument eingefügt werden kann, muss es importiert werden. Beim Import werden dokumentspezifische Eigenschaften wie Verweise auf Stile und Listen vom Original in das importierende Dokument übersetzt. Nachdem der Knoten importiert wurde, kann er mit an der entsprechenden Stelle im Dokument eingefügt werden[`InsertBefore`](../../compositenode/insertbefore) oder [`InsertAfter`](../../compositenode/insertafter).

Wenn der Quellknoten bereits zum Zieldokument gehört, wird einfach ein tiefer Klon des Quellknotens erstellt.

### Beispiele

Zeigt, wie ein Knoten von einem Dokument in ein anderes importiert wird.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// Jeder Knoten hat ein übergeordnetes Dokument, das ist das Dokument, das den Knoten enthält.
// Das Einfügen eines Knotens in ein Dokument, zu dem der Knoten nicht gehört, löst eine Ausnahme aus.
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => { dstDoc.AppendChild(srcDoc.FirstSection); });

// Verwenden Sie die ImportNode-Methode, um eine Kopie eines Knotens zu erstellen, der das Dokument enthalten wird
// die die ImportNode-Methode aufgerufen hat, die als neues Eigentümerdokument festgelegt wurde.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true);

Assert.AreEqual(dstDoc, importedSection.Document);

// Jetzt können wir den Knoten in das Dokument einfügen.
dstDoc.AppendChild(importedSection);

Assert.AreEqual("Destination document first paragraph text.\r\nSource document first paragraph text.\r\n",
    dstDoc.ToString(SaveFormat.Text));
```

### Siehe auch

* class [Node](../../node)
* class [DocumentBase](../../documentbase)
* namensraum [Aspose.Words](../../documentbase)
* Montage [Aspose.Words](../../../)

---

## ImportNode(Node, bool, ImportFormatMode) {#importnode_1}

Importiert einen Knoten aus einem anderen Dokument in das aktuelle Dokument mit einer Option zur Steuerung der Formatierung.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren, ImportFormatMode importFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcNode | Node | Der zu importierende Knoten. |
| isImportChildren | Boolean | True, um alle untergeordneten Knoten rekursiv zu importieren; andernfalls falsch. |
| importFormatMode | ImportFormatMode | Gibt an, wie kollidierende Stilformatierungen zusammengeführt werden. |

### Rückgabewert

Der geklonte, importierte Knoten. Der Knoten gehört zum Zieldokument, hat aber keinen Elternknoten.

### Bemerkungen

Diese Überladung ist nützlich, um zu steuern, wie Stile und Listenformatierungen importiert werden.

Beim Importieren eines Knotens wird eine Kopie des Quellknotens erstellt, der zum importierenden Dokument gehört. Der zurückgegebene Knoten hat keinen Elternknoten. Der Quellknoten wird nicht geändert oder aus dem Originaldokument entfernt.

Bevor ein Knoten aus einem anderen Dokument in dieses Dokument eingefügt werden kann, muss es importiert werden. Beim Import werden dokumentspezifische Eigenschaften wie Verweise auf Stile und Listen vom Original in das importierende Dokument übersetzt. Nachdem der Knoten importiert wurde, kann er mit an der entsprechenden Stelle im Dokument eingefügt werden[`InsertBefore`](../../compositenode/insertbefore) oder [`InsertAfter`](../../compositenode/insertafter).

Wenn der Quellknoten bereits zum Zieldokument gehört, wird einfach ein tiefer Klon des Quellknotens erstellt.

### Beispiele

Zeigt, wie Knoten aus dem Quelldokument in das Zieldokument mit bestimmten Optionen importiert werden.

```csharp
// Zwei Dokumente erstellen und jedem Dokument einen Zeichenstil hinzufügen.
// Konfigurieren Sie die Stile so, dass sie denselben Namen, aber unterschiedliche Textformatierung haben.
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

// Importiere den Abschnitt aus dem Zieldokument in das Quelldokument, was zu einer Namenskollision des Stils führt.
// Wenn wir Zielstile verwenden, dann der importierte Quelltext mit demselben Stilnamen
// als Zieltext übernimmt den Zielstil.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// Wenn wir ImportFormatMode.KeepDifferentStyles verwenden, wird der Quellstil beibehalten,
// und der Namenskonflikt wird durch Hinzufügen eines Suffixes aufgelöst.
dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.KeepDifferentStyles);
Assert.AreEqual(dstStyle.Font.Name, dstDoc.Styles["My style"].Font.Name);
Assert.AreEqual(srcStyle.Font.Name, dstDoc.Styles["My style_0"].Font.Name);
```

### Siehe auch

* class [Node](../../node)
* enum [ImportFormatMode](../../importformatmode)
* class [DocumentBase](../../documentbase)
* namensraum [Aspose.Words](../../documentbase)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
