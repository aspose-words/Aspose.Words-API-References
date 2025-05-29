---
title: ImportFormatOptions.KeepSourceNumbering
linktitle: KeepSourceNumbering
articleTitle: KeepSourceNumbering
second_title: Aspose.Words für .NET
description: Steuern Sie die Dokumentnummerierung mit der Eigenschaft „ImportFormatOptions KeepSourceNumbering“. Beheben Sie Konflikte ganz einfach für nahtlose Importe. Standardwert: „false“.
type: docs
weight: 60
url: /de/net/aspose.words/importformatoptions/keepsourcenumbering/
---
## ImportFormatOptions.KeepSourceNumbering property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, wie die Nummerierung importiert wird, wenn sie in Quell- und Zieldokumenten kollidiert. Der Standardwert ist`FALSCH` .

```csharp
public bool KeepSourceNumbering { get; set; }
```

## Beispiele

Zeigt, wie ein Konflikt beim Importieren von Dokumenten gelöst wird, die Listen mit derselben Listendefinitionskennung enthalten.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Setzen Sie die Eigenschaft „KeepSourceNumbering“ auf „true“, um eine andere Listendefinitions-ID anzuwenden
// in identische Stile, während Aspose.Words sie in Zieldokumente importiert.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

Zeigt, wie ein Dokument mit nummerierten Listen importiert wird.

```csharp
Document srcDoc = new Document(MyDir + "List source.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

Assert.AreEqual(4, dstDoc.Lists.Count);

ImportFormatOptions options = new ImportFormatOptions();

// Wenn es zu einem Konflikt zwischen Listenstilen kommt, wenden Sie das Listenformat des Quelldokuments an.
// Setzen Sie die Eigenschaft „KeepSourceNumbering“ auf „false“, um keine Listennummern in das Zieldokument zu importieren.
// Setzen Sie die Eigenschaft "KeepSourceNumbering" auf "true" und importieren Sie alle
// Nummerierung im Listenstil mit demselben Erscheinungsbild wie im Quelldokument.
options.KeepSourceNumbering = isKeepSourceNumbering;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);
dstDoc.UpdateListLabels();

Assert.AreEqual(isKeepSourceNumbering ? 5 : 4, dstDoc.Lists.Count);
```

Zeigt, wie Konflikte bei der Listennummerierung in Quell- und Zieldokumenten gelöst werden.

```csharp
// Öffnen Sie ein Dokument mit einem benutzerdefinierten Listennummerierungsschema und klonen Sie es dann.
// Da beide das gleiche Nummerierungsformat haben, kommt es zu Konflikten zwischen den Formaten, wenn wir ein Dokument in das andere importieren.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Wenn wir den Klon des Dokuments in das Original importieren und ihn dann anhängen,
// dann werden die beiden Listen mit demselben Listenformat verbunden.
// Wenn wir das Flag "KeepSourceNumbering" auf "false" setzen, dann wird die Liste aus dem Dokumentklon
// die wir an das Original anhängen, übernehmen die Nummerierung der Liste, an die wir sie anhängen.
// Dadurch werden die beiden Listen effektiv zu einer zusammengeführt.
// Wenn wir das Flag "KeepSourceNumbering" auf "true" setzen, dann wird der Dokumentklon
    // Die Liste behält ihre ursprüngliche Nummerierung bei, sodass die beiden Listen als separate Listen angezeigt werden.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.KeepSourceNumbering = keepSourceNumbering;

NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepDifferentStyles, importFormatOptions);
foreach (Paragraph paragraph in srcDoc.FirstSection.Body.Paragraphs)
{
    Node importedNode = importer.ImportNode(paragraph, true);
    dstDoc.FirstSection.Body.AppendChild(importedNode);
}

dstDoc.UpdateListLabels();

if (keepSourceNumbering)
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
else
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
```

### Siehe auch

* class [ImportFormatOptions](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
