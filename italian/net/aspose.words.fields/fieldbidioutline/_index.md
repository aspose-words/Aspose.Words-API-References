---
title: FieldBidiOutline Class
linktitle: FieldBidiOutline
articleTitle: FieldBidiOutline
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldBidiOutline per un'implementazione fluida del campo BIDIOUTLINE, migliorando le capacità di elaborazione dei documenti.
type: docs
weight: 2060
url: /it/net/aspose.words.fields/fieldbidioutline/
---
## FieldBidiOutline class

Implementa il campo BIDIOUTLINE.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldBidiOutline : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldBidiOutline](fieldbidioutline/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene un[`FieldFormat`](../fieldformat/)oggetto che fornisce accesso tipizzato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ottiene il tipo di campo di Microsoft Word. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). Sono inclusi sia il codice di campo che il risultato del campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo nodo figlio del suo nodo padre, restituisce il paragrafo padre. Se il campo è già stato rimosso, restituisce`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Esegue l'aggiornamento del campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Esegue un aggiornamento di campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |

## Osservazioni

Questo campo è identico al campo AUTONUMLGL, ad eccezione del separatore che delimita ogni livello della numerazione dei paragrafi.

## Esempi

Mostra come creare elenchi compatibili con le lingue con scrittura da destra a sinistra con campi BIDIOUTLINE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Il campo BIDIOUTLINE numera i paragrafi come i campi AUTONUM/LISTNUM,
// ma è visibile solo quando è abilitata una lingua di modifica da destra a sinistra, come l'ebraico o l'arabo.
// Il campo seguente visualizzerà ".1", l'equivalente RTL del numero di elenco "1.".
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// Aggiungere altri due campi BIDIOUTLINE, che visualizzeranno ".2" e ".3".
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// Imposta l'allineamento orizzontale del testo per ogni paragrafo del documento su RTL.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// Se abilitiamo una lingua di modifica da destra a sinistra in Microsoft Word, i nostri campi visualizzeranno numeri.
// Altrimenti verrà visualizzato "###".
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
