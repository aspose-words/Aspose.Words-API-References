---
title: FieldPrint.PostScriptGroup
linktitle: PostScriptGroup
articleTitle: PostScriptGroup
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldPrint PostScriptGroup-Eigenschaft, um Ihr Zeichenrechteck für eine effiziente Verarbeitung von PostScript-Anweisungen einfach zu verwalten.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldprint/postscriptgroup/
---
## FieldPrint.PostScriptGroup property

Ruft das Zeichenrechteck ab, auf das die PostScript-Anweisungen angewendet werden, oder legt dieses fest.

```csharp
public string PostScriptGroup { get; set; }
```

## Beispiele

Zeigt das Einfügen eines PRINT-Felds.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// Das Feld PRINT kann Anweisungen an den Drucker senden.
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// Legen Sie den Bereich fest, in dem der Drucker Anweisungen ausführen soll.
// In diesem Fall ist es der Absatz, der unser PRINT-Feld enthält.
field.PostScriptGroup = "para";

// Wenn wir zum Drucken unseres Dokuments einen Drucker verwenden, der PostScript unterstützt,
// Dieser Befehl färbt den gesamten Bereich, den wir in „field.PostScriptGroup“ angegeben haben, weiß.
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### Siehe auch

* class [FieldPrint](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
