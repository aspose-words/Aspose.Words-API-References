---
title: FieldSymbol.CharacterCode
second_title: Aspose.Words per .NET API Reference
description: FieldSymbol proprietà. Ottiene o imposta il valore del punto di codice del carattere in decimale o esadecimale.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldsymbol/charactercode/
---
## FieldSymbol.CharacterCode property

Ottiene o imposta il valore del punto di codice del carattere in decimale o esadecimale.

```csharp
public string CharacterCode { get; set; }
```

### Esempi

Mostra come utilizzare il campo SIMBOLO.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati tre modi per utilizzare un campo SIMBOLO per visualizzare un singolo carattere.
// 1 - Aggiungi un campo SIMBOLO che visualizza il simbolo © (Copyright), specificato da un codice carattere ANSI:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// Il codice carattere ANSI "U+00A9", o "169" in formato intero, è riservato al simbolo del copyright.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - Aggiungi un campo SIMBOLO che visualizzi il simbolo ∞ (Infinito) e modifica il suo aspetto:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// In Unicode, il simbolo dell'infinito occupa il codice "221E".
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// Cambia il carattere del nostro simbolo dopo aver utilizzato la mappa caratteri di Windows
// per garantire che il carattere possa rappresentare quel simbolo.
field.FontName = "Calibri";
field.FontSize = "24";

// Possiamo impostare questo flag per i simboli alti per fare in modo che non spingano verso il basso il resto del testo sulla loro riga.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - Aggiungi un campo SIMBOLO che visualizzi il carattere あ,
// con un carattere che supporta la codepage Shift-JIS (Windows-932):
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);
field.FontName = "MS Gothic";
field.CharacterCode = 0x82A0.ToString();
field.IsShiftJis = true;

Assert.AreEqual(" SYMBOL  33440 \\f \"MS Gothic\" \\j", field.GetFieldCode());

builder.Write("Line 3");

doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### Guarda anche

* class [FieldSymbol](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldsymbol/)
* assemblea [Aspose.Words](../../../)


