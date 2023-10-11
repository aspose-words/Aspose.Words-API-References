---
title: FieldPrint.PrinterInstructions
second_title: Aspose.Words für .NET-API-Referenz
description: FieldPrint eigendom. Ruft die druckerspezifischen Steuercodezeichen oder PostScriptAnweisungen ab oder legt diese fest.
type: docs
weight: 30
url: /de/net/aspose.words.fields/fieldprint/printerinstructions/
---
## FieldPrint.PrinterInstructions property

Ruft die druckerspezifischen Steuercodezeichen oder PostScript-Anweisungen ab oder legt diese fest.

```csharp
public string PrinterInstructions { get; set; }
```

### Beispiele

Zeigt an, wie ein PRINT-Feld eingefügt werden soll.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// Das PRINT-Feld kann Anweisungen an den Drucker senden.
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
* namensraum [Aspose.Words.Fields](../../fieldprint/)
* Montage [Aspose.Words](../../../)


