---
title: DocumentBuilder.InsertDocument
linktitle: InsertDocument
articleTitle: InsertDocument
second_title: Aspose.Words für .NET
description: Fügen Sie mit der InsertDocument-Methode von DocumentBuilder mühelos Dokumente an jeder Cursorposition ein. Optimieren Sie Ihren Workflow und steigern Sie Ihre Produktivität!
type: docs
weight: 310
url: /de/net/aspose.words/documentbuilder/insertdocument/
---
## InsertDocument(*[Document](../../document/), [ImportFormatMode](../../importformatmode/)*) {#insertdocument}

Fügt ein Dokument an der Cursorposition ein.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcDoc | Document | Quelldokument zum Einfügen. |
| importFormatMode | ImportFormatMode | Gibt an, wie kollidierende Stilformatierungen zusammengeführt werden. |

### Rückgabewert

Erster Knoten des eingefügten Inhalts.

## Bemerkungen

Diese Methode imitiert das Verhalten von MS Word, als ob STRG+'A' (gesamten Inhalt auswählen) gedrückt würde, dann STRG+'C' (Auswahl in den Puffer kopieren) innerhalb eines Dokuments und dann STRG+'V' (Inhalt aus dem Puffer einfügen) innerhalb eines anderen Dokuments.

## Beispiele

Zeigt, wie ein Dokument in ein anderes Dokument eingefügt wird.

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### Siehe auch

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## InsertDocument(*[Document](../../document/), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#insertdocument_1}

Fügt ein Dokument an der Cursorposition ein.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode, 
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

## Beispiele

Zeigt, wie doppelte Stile beim Einfügen von Dokumenten aufgelöst werden.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Klonen Sie das Dokument und bearbeiten Sie den „MyStyle“-Stil des Klons, sodass er eine andere Farbe als das Original hat.
// Wenn wir den Klon in das Originaldokument einfügen, kommt es aufgrund der beiden gleichnamigen Stile zu einem Konflikt.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// Wenn wir SmartStyleBehavior aktivieren und den KeepSourceFormatting-Importformatmodus verwenden,
// Aspose.Words löst Stilkonflikte durch Konvertieren der Quelldokumentstile.
// mit denselben Namen wie Zielstile in direkte Absatzattribute.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Siehe auch

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
