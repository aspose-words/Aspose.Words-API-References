---
title: FieldPrint.PrinterInstructions
linktitle: PrinterInstructions
articleTitle: PrinterInstructions
second_title: Aspose.Words per .NET
description: Scopri come gestire i codici di controllo specifici della stampante e le istruzioni PostScript con FieldPrint PrinterInstructions per soluzioni di stampa ottimizzate.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldprint/printerinstructions/
---
## FieldPrint.PrinterInstructions property

Ottiene o imposta i caratteri del codice di controllo specifici della stampante o le istruzioni PostScript.

```csharp
public string PrinterInstructions { get; set; }
```

## Esempi

Mostra come inserire un campo STAMPA.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// Il campo PRINT può inviare istruzioni alla stampante.
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// Imposta l'area su cui la stampante dovrà eseguire le istruzioni.
// In questo caso, sarà il paragrafo a contenere il nostro campo PRINT.
field.PostScriptGroup = "para";

// Quando utilizziamo una stampante che supporta PostScript per stampare il nostro documento,
// questo comando renderà bianca l'intera area specificata in "field.PostScriptGroup".
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### Guarda anche

* class [FieldPrint](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
