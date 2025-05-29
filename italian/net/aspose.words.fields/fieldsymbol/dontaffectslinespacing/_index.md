---
title: FieldSymbol.DontAffectsLineSpacing
linktitle: DontAffectsLineSpacing
articleTitle: DontAffectsLineSpacing
second_title: Aspose.Words per .NET
description: Scopri come la proprietà FieldSymbol DontAffectsLineSpacing controlla l'impatto del carattere sull'interlinea del paragrafo. Ottimizza la formattazione del tuo documento oggi stesso!
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldsymbol/dontaffectslinespacing/
---
## FieldSymbol.DontAffectsLineSpacing property

Ottiene o imposta se il carattere recuperato dal campo influisce sulla spaziatura delle righe del paragrafo.

```csharp
public bool DontAffectsLineSpacing { get; set; }
```

## Esempi

Mostra come utilizzare il campo SIMBOLO.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati tre modi per utilizzare un campo SYMBOL per visualizzare un singolo carattere.
// 1 - Aggiungere un campo SIMBOLO che visualizzi il simbolo © (Copyright), specificato da un codice carattere ANSI:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// Il codice carattere ANSI "U+00A9", ovvero "169" in formato intero, è riservato al simbolo di copyright.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - Aggiungere un campo SIMBOLO che visualizzi il simbolo ∞ (infinito) e modificarne l'aspetto:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// In Unicode, il simbolo di infinito occupa il codice "221E".
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// Cambia il font del nostro simbolo dopo aver utilizzato la mappa dei caratteri di Windows
// per garantire che il font possa rappresentare quel simbolo.
field.FontName = "Calibri";
field.FontSize = "24";

// Possiamo impostare questo flag per i simboli alti in modo che non spingano verso il basso il resto del testo sulla loro riga.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - Aggiungi un campo SIMBOLO che visualizza il carattere あ,
// con un font che supporta la codepage Shift-JIS (Windows-932):
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
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
