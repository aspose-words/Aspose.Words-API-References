---
title: FieldSymbol
second_title: Aspose.Words per .NET API Reference
description: Implementa un campo SYMBOL.
type: docs
weight: 2310
url: /it/net/aspose.words.fields/fieldsymbol/
---
## FieldSymbol class

Implementa un campo SYMBOL.

```csharp
public class FieldSymbol : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldSymbol](fieldsymbol)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CharacterCode](../../aspose.words.fields/fieldsymbol/charactercode) { get; set; } | Ottiene o imposta il valore del punto di codice del carattere in decimale o esadecimale. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [DontAffectsLineSpacing](../../aspose.words.fields/fieldsymbol/dontaffectslinespacing) { get; set; } | Ottiene o imposta se il carattere recuperato dal campo influisce sull'interlinea del paragrafo. |
| [End](../../aspose.words.fields/field/end) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [FontName](../../aspose.words.fields/fieldsymbol/fontname) { get; set; } | Ottiene o imposta il nome del font del carattere recuperato dal campo. |
| [FontSize](../../aspose.words.fields/fieldsymbol/fontsize) { get; set; } | Ottiene o imposta la dimensione in punti del font del carattere recuperato dal campo. |
| [Format](../../aspose.words.fields/field/format) { get; } | Ottiene a[`FieldFormat`](../fieldformat) oggetto che fornisce l'accesso digitato alla formattazione del campo. |
| [IsAnsi](../../aspose.words.fields/fieldsymbol/isansi) { get; set; } | Ottiene o imposta se il codice del carattere viene interpretato come il valore di un carattere ANSI. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolarne il risultato). |
| [IsShiftJis](../../aspose.words.fields/fieldsymbol/isshiftjis) { get; set; } | Ottiene o imposta se il codice carattere viene interpretato come il valore di un carattere SHIFT-JIS. |
| [IsUnicode](../../aspose.words.fields/fieldsymbol/isunicode) { get; set; } | Ottiene o imposta se il codice carattere viene interpretato come il valore di un carattere Unicode. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Ottiene o imposta il testo che si trova tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere nullo. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ottiene il tipo di campo di Microsoft Word. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice campo che il risultato campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). |
| [Remove](../../aspose.words.fields/field/remove)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo padre, restituisce il suo paragrafo padre. Se il campo è già stato rimosso, ritorna **nullo** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update)() | Esegue l'aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update)(bool) | Esegue un aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |

### Osservazioni

Recupera il carattere il cui valore del punto di codice è specificato in decimale o esadecimale.

### Esempi

Mostra come utilizzare il campo SIMBOLO.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati tre modi per utilizzare un campo SYMBOL per visualizzare un singolo carattere.
// 1 - Aggiungi un campo SYMBOL che visualizza il simbolo © (Copyright), specificato da un codice carattere ANSI:
FieldSymbol field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// Il codice carattere ANSI "U+00A9", o "169" in forma intera, è riservato al simbolo del copyright.
field.CharacterCode = 0x00a9.ToString();
field.IsAnsi = true;

Assert.AreEqual(" SYMBOL  169 \\a", field.GetFieldCode());

builder.Writeln(" Line 1");

// 2 - Aggiungi un campo SYMBOL che visualizza il simbolo ∞ (Infinito) e modifica il suo aspetto:
field = (FieldSymbol)builder.InsertField(FieldType.FieldSymbol, true);

// In Unicode, il simbolo dell'infinito occupa il codice "221E".
field.CharacterCode = 0x221E.ToString();
field.IsUnicode = true;

// Cambia il carattere del nostro simbolo dopo aver utilizzato la Mappa caratteri di Windows
// per garantire che il carattere possa rappresentare quel simbolo.
field.FontName = "Calibri";
field.FontSize = "24";

// Possiamo impostare questo flag per i simboli alti in modo che non spingano verso il basso il resto del testo sulla loro riga.
field.DontAffectsLineSpacing = true;

Assert.AreEqual(" SYMBOL  8734 \\u \\f Calibri \\s 24 \\h", field.GetFieldCode());

builder.Writeln("Line 2");

// 3 - Aggiungi un campo SYMBOL che visualizza il carattere あ,
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

* class [Field](../field)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
