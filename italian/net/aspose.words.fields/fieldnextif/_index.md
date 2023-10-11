---
title: Class FieldNextIf
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fields.FieldNextIf classe. Implementa il campo NEXTIF.
type: docs
weight: 2190
url: /it/net/aspose.words.fields/fieldnextif/
---
## FieldNextIf class

Implementa il campo NEXTIF.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldNextIf : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldNextIf](fieldnextif/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldnextif/comparisonoperator/) { get; set; } | Ottiene o imposta l'operatore di confronto. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene a[`FieldFormat`](../fieldformat/) oggetto che fornisce accesso digitato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non deve ricalcolare il risultato). |
| [LeftExpression](../../aspose.words.fields/fieldnextif/leftexpression/) { get; set; } | Ottiene o imposta la parte sinistra dell'espressione di confronto. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo. |
| [RightExpression](../../aspose.words.fields/fieldnextif/rightexpression/) { get; set; } | Ottiene o imposta la parte destra dell'espressione di confronto. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere`nullo` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
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

### Osservazioni

Confronta i valori designati dalle espressioni[`LeftExpression`](./leftexpression/) E[`RightExpression`](./rightexpression/) in confronto utilizzando l'operatore designato da[`ComparisonOperator`](./comparisonoperator/) . Se il confronto è vero, il record di dati successivo viene unito al documento di unione corrente. (I campi di unione che seguono NEXTIF nel documento main vengono sostituiti dai valori del record di dati successivo anziché dal record di dati corrente.) Se il confronto è falso, il record di dati successivo viene unito in un nuovo documento di unione.

### Esempi

Mostra come utilizzare i campi NEXT/NEXTIF per unire più righe in un'unica pagina durante una stampa unione.

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Crea un'origine dati per la nostra stampa unione con 3 righe.
    // Una stampa unione che utilizza questa tabella creerebbe normalmente un documento di 3 pagine.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // Se abbiamo più campi di unione con lo stesso FieldName,
    // riceveranno i dati dalla stessa riga dell'origine dati e visualizzeranno lo stesso valore dopo l'unione.
    // Un campo NEXT indica immediatamente alla stampa unione di spostarsi di una riga verso il basso,
    // il che significa che tutti i MERGEFIELD che seguono il campo NEXT riceveranno i dati dalla riga successiva.
    // Assicurati di non provare mai a saltare alla riga successiva mentre sei già sull'ultima riga.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // Dopo l'unione, i valori dell'origine dati accettati da questi MERGEFIELD
     // finirà sulla stessa pagina dei MERGEFIELD sopra.
    InsertMergeFields(builder, "Second row: ");

    // Un campo NEXTIF ha la stessa funzione di un campo NEXT,
    // ma salta alla riga successiva solo se un'istruzione costruita dalle seguenti 3 proprietà è vera.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // Se il confronto affermato dal campo precedente è corretto,
    // i seguenti 3 campi di unione prenderanno i dati dalla terza riga.
    // Altrimenti, questi campi prenderanno nuovamente i dati dalla riga 2.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     // La nostra origine dati ha 3 righe e le abbiamo saltate due volte.
    // Il nostro documento di output avrà 1 pagina con i dati di tutte e 3 le righe.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

/// <summary>
/// Utilizza un generatore di documenti per inserire MERGEFIELD per un'origine dati che contiene colonne denominate "Titolo di cortesia", "Nome" e "Cognome".
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// Utilizza un generatore di documenti per inserire un MERRGEFIELD con le proprietà specificate.
/// </summary>
public void InsertMergeField(DocumentBuilder builder, string fieldName, string textBefore, string textAfter)
{
    FieldMergeField field = (FieldMergeField) builder.InsertField(FieldType.FieldMergeField, true);
    field.FieldName = fieldName;
    field.TextBefore = textBefore;
    field.TextAfter = textAfter;
}
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)


