---
title: StyleCollection.AddCopy
linktitle: AddCopy
articleTitle: AddCopy
second_title: Aspose.Words für .NET
description: Kopieren Sie Stile mühelos mit der AddCopy-Methode von StyleCollection. Verbessern Sie Ihren Design-Workflow und optimieren Sie Ihr Stilmanagement!
type: docs
weight: 70
url: /de/net/aspose.words/stylecollection/addcopy/
---
## StyleCollection.AddCopy method

Kopiert einen Stil in diese Sammlung.

```csharp
public Style AddCopy(Style style)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| style | Style | Zu kopierender Stil. |

### Rückgabewert

Kopierter Stil, einsatzbereit.

## Bemerkungen

Der zu kopierende Stil kann sowohl zum selben als auch zu einem anderen Dokument gehören.

Verknüpfter Stil wird kopiert.

Diese Methode kopiert keine Basisstile.

Wenn die Sammlung bereits einen Stil mit dem gleichen Namen enthält, wird der neue Name automatisch generiert, indem das Suffix "_number" hinzugefügt wird, beginnend bei 0, z. B. "Normal_0", "Überschrift 1_1" usw. Verwenden[`Name`](../../style/name/) Setter zum Ändern des Namens des importierten Stils.

## Beispiele

Zeigt, wie ein Stil aus einem Dokument in ein anderes Dokument importiert wird.

```csharp
Document srcDoc = new Document();

// Erstellen Sie einen benutzerdefinierten Stil für das Quelldokument.
Style srcStyle = srcDoc.Styles.Add(StyleType.Paragraph, "MyStyle");
srcStyle.Font.Color = Color.Red;

// Importieren Sie den benutzerdefinierten Stil des Quelldokuments in das Zieldokument.
Document dstDoc = new Document();
Style newStyle = dstDoc.Styles.AddCopy(srcStyle);

// Der importierte Stil hat ein mit dem Quellstil identisches Erscheinungsbild.
Assert.AreEqual("MyStyle", newStyle.Name);
Assert.AreEqual(Color.Red.ToArgb(), newStyle.Font.Color.ToArgb());
```

Zeigt, wie der Stil eines Dokuments geklont wird.

```csharp
Document doc = new Document();

// Die AddCopy-Methode erstellt eine Kopie des angegebenen Stils und
// generiert automatisch einen neuen Namen für den Stil, beispielsweise „Überschrift 1_0“.
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

// Verwenden Sie die Eigenschaft „Name“ des Stils, um den identifizierenden Namen des Stils zu ändern.
newStyle.Name = "My Heading 1";

// Unser Dokument hat jetzt zwei identisch aussehende Stile mit unterschiedlichen Namen.
// Das Ändern der Einstellungen eines der Stile wirkt sich nicht auf den anderen aus.
newStyle.Font.Color = Color.Red;

Assert.AreEqual("My Heading 1", newStyle.Name);
Assert.AreEqual("Heading 1", doc.Styles["Heading 1"].Name);

Assert.AreEqual(doc.Styles["Heading 1"].Type, newStyle.Type);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Name, newStyle.Font.Name);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Size, newStyle.Font.Size);
Assert.AreNotEqual(doc.Styles["Heading 1"].Font.Color, newStyle.Font.Color);
```

### Siehe auch

* class [Style](../../style/)
* class [StyleCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
