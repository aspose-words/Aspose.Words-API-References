---
title: FieldPrint.PostScriptGroup
linktitle: PostScriptGroup
articleTitle: PostScriptGroup
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldPrint PostScriptGroup per gestire facilmente il rettangolo di disegno per una gestione efficiente delle istruzioni PostScript.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldprint/postscriptgroup/
---
## FieldPrint.PostScriptGroup property

Ottiene o imposta il rettangolo di disegno su cui operano le istruzioni PostScript.

```csharp
public string PostScriptGroup { get; set; }
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
