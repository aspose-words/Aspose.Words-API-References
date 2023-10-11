---
title: DocumentBuilder.InsertDocument
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Fügt ein Dokument an der Cursorposition ein.
type: docs
weight: 310
url: /de/net/aspose.words/documentbuilder/insertdocument/
---
## InsertDocument(Document, ImportFormatMode) {#insertdocument}

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

### Bemerkungen

Diese Methode ahmt das Verhalten von MS Word nach, als ob STRG+'A' (alle Inhalte auswählen) gedrückt würde, dann STRG+'C' (Ausgewählte in den Puffer kopieren) innerhalb eines Dokuments und dann STRG+'V' (Inhalt aus dem einfügen). Puffer) in einem anderen Dokument.

### Beispiele

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
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)

---

## InsertDocument(Document, ImportFormatMode, ImportFormatOptions) {#insertdocument_1}

Fügt ein Dokument an der Cursorposition ein.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcDoc | Document | Quelldokument zum Einfügen. |
| importFormatMode | ImportFormatMode | Gibt an, wie kollidierende Stilformatierungen zusammengeführt werden. |
| importFormatOptions | ImportFormatOptions | Ermöglicht die Angabe von Optionen, die sich auf die Formatierung eines Ergebnisdokuments auswirken. |

### Rückgabewert

Erster Knoten des eingefügten Inhalts.

### Bemerkungen

Diese Methode ahmt das Verhalten von MS Word nach, als ob STRG+'A' (alle Inhalte auswählen) gedrückt würde, dann STRG+'C' (Ausgewählte in den Puffer kopieren) innerhalb eines Dokuments und dann STRG+'V' (Inhalt aus dem einfügen). Puffer) in einem anderen Dokument.

### Beispiele

Zeigt, wie du doppelte Stile beim Einfügen von Dokumenten auflöst.

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
// Wenn wir den Klon in das Originaldokument einfügen, kommt es zu einem Konflikt zwischen den beiden Stilen mit demselben Namen.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// Wenn wir SmartStyleBehavior aktivieren und den Importformatmodus KeepSourceFormatting verwenden,
// Aspose.Words löst Stilkonflikte durch Konvertieren von Quelldokumentstilen.
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
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


