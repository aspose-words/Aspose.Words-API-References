---
title: DocumentBuilder.InsertDocumentInline
linktitle: InsertDocumentInline
articleTitle: InsertDocumentInline
second_title: Aspose.Words für .NET
description: Fügen Sie mit der InsertDocumentInline-Methode von DocumentBuilder mühelos Dokumente inline ein und verbessern Sie so Ihren Arbeitsablauf und die Dokumentbearbeitung.
type: docs
weight: 320
url: /de/net/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder.InsertDocumentInline method

Fügt ein Dokument inline an der Cursorposition ein.

```csharp
public Node InsertDocumentInline(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcDoc | Document | Quelldokument zum Einfügen. |
| importFormatMode | ImportFormatMode | Gibt an, wie kollidierende Stilformatierungen zusammengeführt werden. |
| importFormatOptions | ImportFormatOptions | Ermöglicht die Angabe von Optionen, die die Formatierung eines Ergebnisdokuments beeinflussen. |

### Rückgabewert

Erster Knoten des eingefügten Inhalts.

## Bemerkungen

Diese Methode imitiert das Verhalten von MS Word, als ob STRG+'A' (gesamten Inhalt auswählen) gedrückt würde, dann STRG+'C' (Auswahl in den Puffer kopieren) innerhalb eines Dokuments und dann STRG+'V' (Inhalt aus dem Puffer einfügen) innerhalb eines anderen Dokuments.

Im Unterschied zu[`InsertDocument`](../insertdocument/) Diese Methode verschiebt den Inhalt des Absatzes des Zieldokuments, vor dem das Quelldokument eingefügt wurde, in den letzten Absatz des eingefügten Quelldokuments. Konkret bedeutet dies, dass der Absatzumbruch des zuletzt eingefügten Absatzes entfernt wird.

Beachten Sie: Wenn der letzte Knoten des Quelldokuments kein Absatz ist, wird nichts unternommen.

## Beispiele

Zeigt, wie ein Dokument inline an der Cursorposition eingefügt wird.

```csharp
DocumentBuilder srcDoc = new DocumentBuilder();
srcDoc.Write("[src content]");

// Zieldokument erstellen.
DocumentBuilder dstDoc = new DocumentBuilder();
dstDoc.Write("Before ");
dstDoc.InsertNode(new BookmarkStart(dstDoc.Document, "src_place"));
dstDoc.InsertNode(new BookmarkEnd(dstDoc.Document, "src_place"));
dstDoc.Write(" after");

Assert.AreEqual("Before  after", dstDoc.Document.GetText().TrimEnd());

// Quelldokument inline in Ziel einfügen.
dstDoc.MoveToBookmark("src_place");
dstDoc.InsertDocumentInline(srcDoc.Document, ImportFormatMode.UseDestinationStyles, new ImportFormatOptions());

Assert.AreEqual("Before [src content] after", dstDoc.Document.GetText().TrimEnd());
```

### Siehe auch

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
