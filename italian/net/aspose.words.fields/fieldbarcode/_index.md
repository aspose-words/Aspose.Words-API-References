---
title: FieldBarcode
second_title: Aspose.Words per .NET API Reference
description: Implementa il campo BARCODE.
type: docs
weight: 1480
url: /it/net/aspose.words.fields/fieldbarcode/
---
## FieldBarcode class

Implementa il campo BARCODE.

```csharp
public class FieldBarcode : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldBarcode](fieldbarcode)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [FacingIdentificationMark](../../aspose.words.fields/fieldbarcode/facingidentificationmark) { get; set; } | Ottiene o imposta il tipo di FIM (Facing Identification Mark) da inserire. |
| [Format](../../aspose.words.fields/field/format) { get; } | Ottiene a[`FieldFormat`](../fieldformat) oggetto che fornisce l'accesso digitato alla formattazione del campo. |
| [IsBookmark](../../aspose.words.fields/fieldbarcode/isbookmark) { get; set; } | Ottiene o imposta se[`PostalAddress`](./postaladdress) è il nome di un segnalibro. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolarne il risultato). |
| [IsUSPostalAddress](../../aspose.words.fields/fieldbarcode/isuspostaladdress) { get; set; } | Ottiene o imposta se[`PostalAddress`](./postaladdress) è un indirizzo postale statunitense. |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [PostalAddress](../../aspose.words.fields/fieldbarcode/postaladdress) { get; set; } | Ottiene o imposta l'indirizzo postale utilizzato per la generazione di un codice a barre o il nome del segnalibro che fa riferimento ad esso. |
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

Inserisce un codice a barre postale in un formato di indirizzo leggibile dalla macchina utilizzato dal servizio postale degli Stati Uniti.

### Esempi

Mostra come utilizzare il campo CODICE A BARRE per visualizzare i codici postali statunitensi sotto forma di codice a barre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Di seguito sono riportati due modi per utilizzare i campi CODICE A BARRE per visualizzare valori personalizzati come codici a barre.
// 1 - Memorizza il valore che il codice a barre visualizzerà nella proprietà PostalAddress:
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// Questo valore deve essere un codice postale valido.
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 - Fare riferimento a un segnalibro che memorizza il valore che verrà visualizzato da questo codice a barre:
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// Il segnalibro a cui fa riferimento il campo BARCODE nella relativa proprietà PostalAddress
// non deve contenere nulla oltre al codice postale valido.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("BarcodeBookmark");
builder.Writeln("968877");
builder.EndBookmark("BarcodeBookmark");

doc.Save(ArtifactsDir + "Field.BARCODE.docx");
```

### Guarda anche

* class [Field](../field)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
