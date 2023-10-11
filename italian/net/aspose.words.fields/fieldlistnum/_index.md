---
title: Class FieldListNum
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fields.FieldListNum classe. Implementa il campo LISTNUM.
type: docs
weight: 2120
url: /it/net/aspose.words.fields/fieldlistnum/
---
## FieldListNum class

Implementa il campo LISTNUM.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldListNum : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldListNum](fieldlistnum/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene a[`FieldFormat`](../fieldformat/) oggetto che fornisce accesso digitato alla formattazione del campo. |
| [HasListName](../../aspose.words.fields/fieldlistnum/haslistname/) { get; } | Restituisce un valore che indica se il nome di una definizione di numerazione astratta è fornito dal codice del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non deve ricalcolare il risultato). |
| [ListLevel](../../aspose.words.fields/fieldlistnum/listlevel/) { get; set; } | Ottiene o imposta il livello nell'elenco, sovrascrivendo il comportamento predefinito del campo. |
| [ListName](../../aspose.words.fields/fieldlistnum/listname/) { get; set; } | Ottiene o imposta il nome della definizione di numerazione astratta utilizzata per la numerazione. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere`nullo` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| [StartingNumber](../../aspose.words.fields/fieldlistnum/startingnumber/) { get; set; } | Ottiene o imposta il valore iniziale per questo campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ottiene il tipo di campo Microsoft Word. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Restituisce il testo compreso tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice di campo che il risultato del campo dei campi secondari. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce`nullo` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Esegue l'aggiornamento del campo. Genera un risultato se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Esegue un aggiornamento del campo. Genera un risultato se il campo è già in fase di aggiornamento. |

### Esempi

Mostra come numerare i paragrafi con i campi LISTNUM.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// I campi LISTNUM visualizzano un numero che aumenta in ciascun campo LISTNUM.
// Questi campi hanno anche una varietà di opzioni che ci permettono di usarli per emulare elenchi numerati.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Le liste iniziano a contare da 1 per impostazione predefinita, ma possiamo impostare questo numero su un valore diverso, ad esempio 0.
// Questo campo visualizzerà "0)".
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

 // I campi LISTNUM mantengono conteggi separati per ogni livello di elenco.
// Inserimento di un campo LISTNUM nello stesso paragrafo di un altro campo LISTNUM
// aumenta il livello dell'elenco anziché il conteggio.
// Il campo successivo continuerà il conteggio iniziato in precedenza e visualizzerà il valore "1" al livello 1 dell'elenco.
builder.InsertField(FieldType.FieldListNum, true);

// Questo campo inizierà un conteggio al livello 2 dell'elenco. Verrà visualizzato il valore "1".
builder.InsertField(FieldType.FieldListNum, true);

// Questo campo inizierà un conteggio al livello 3 dell'elenco. Verrà visualizzato il valore "1".
// Diversi livelli di elenco hanno una formattazione diversa,
// quindi questi campi combinati visualizzeranno il valore "1)a)i)".
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Il successivo campo LISTNUM che inseriremo continuerà il conteggio a livello di elenco
// che il campo LISTNUM precedente era attivo.
// Possiamo utilizzare la proprietà "ListLevel" per passare a un livello di elenco diverso.
// Se questo campo LISTNUM rimanesse al livello 3 dell'elenco, verrebbe visualizzato "ii)",
// ma, poiché l'abbiamo spostata al livello 2 della lista, continua il conteggio a quel livello e visualizza "b)".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Possiamo impostare la proprietà ListName per fare in modo che il campo emuli un tipo di campo AUTONUM diverso.
// "NumberDefault" emula AUTONUM, "OutlineDefault" emula AUTONUMOUT,
// e "LegalDefault" emula i campi AUTONUMLGL.
// Il nome dell'elenco "OutlineDefault" con 1 come numero iniziale risulterà nella visualizzazione di "I.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// Il ListName non viene trasferito dal campo precedente, quindi dovremo impostarlo per ogni nuovo campo.
// Questo campo continua il conteggio con il nome dell'elenco diverso e visualizza "II.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)


