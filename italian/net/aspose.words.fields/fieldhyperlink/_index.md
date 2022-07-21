---
title: FieldHyperlink
second_title: Aspose.Words per .NET API Reference
description: Implementa il campo HYPERLINK
type: docs
weight: 1840
url: /it/net/aspose.words.fields/fieldhyperlink/
---
## FieldHyperlink class

Implementa il campo HYPERLINK

```csharp
public class FieldHyperlink : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldHyperlink](fieldhyperlink)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Address](../../aspose.words.fields/fieldhyperlink/address) { get; set; } | Ottiene o imposta una posizione in cui questo collegamento ipertestuale salta. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format) { get; } | Ottiene a[`FieldFormat`](../fieldformat) oggetto che fornisce l'accesso digitato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsImageMap](../../aspose.words.fields/fieldhyperlink/isimagemap) { get; set; } | Ottiene o imposta se aggiungere le coordinate al collegamento ipertestuale per una mappa immagine lato server. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolarne il risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [OpenInNewWindow](../../aspose.words.fields/fieldhyperlink/openinnewwindow) { get; set; } | Ottiene o imposta se aprire il sito di destinazione in una nuova finestra del browser web. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Ottiene o imposta il testo che si trova tra il separatore di campo e la fine del campo. |
| [ScreenTip](../../aspose.words.fields/fieldhyperlink/screentip) { get; set; } | Ottiene o imposta il testo della descrizione schermo per il collegamento ipertestuale. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere nullo. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| [SubAddress](../../aspose.words.fields/fieldhyperlink/subaddress) { get; set; } | Ottiene o imposta una posizione nel file, ad esempio un segnalibro, in cui salta questo collegamento ipertestuale. |
| [Target](../../aspose.words.fields/fieldhyperlink/target) { get; set; } | Ottiene o imposta la destinazione a cui reindirizzare il collegamento. |
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

Se selezionato, fa in modo che il controllo salti alla posizione, ad esempio un segnalibro o un URL.

### Esempi

Mostra come utilizzare i campi HYPERLINK per collegarsi a documenti nel file system locale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// Quando facciamo clic su questo campo HYPERLINK in Microsoft Word,
// aprirà il documento collegato e quindi posizionerà il cursore sul segnalibro specificato.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// Quando facciamo clic su questo campo HYPERLINK in Microsoft Word,
// aprirà il documento collegato e scorrerà automaticamente fino all'iframe specificato.
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### Guarda anche

* class [Field](../field)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
