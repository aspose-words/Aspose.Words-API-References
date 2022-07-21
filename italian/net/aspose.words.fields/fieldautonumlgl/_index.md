---
title: FieldAutoNumLgl
second_title: Aspose.Words per .NET API Reference
description: Implementa il campo AUTONUMLGL.
type: docs
weight: 1440
url: /it/net/aspose.words.fields/fieldautonumlgl/
---
## FieldAutoNumLgl class

Implementa il campo AUTONUMLGL.

```csharp
public class FieldAutoNumLgl : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldAutoNumLgl](fieldautonumlgl)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format) { get; } | Ottiene a[`FieldFormat`](../fieldformat) oggetto che fornisce l'accesso digitato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolarne il risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [RemoveTrailingPeriod](../../aspose.words.fields/fieldautonumlgl/removetrailingperiod) { get; set; } | Ottiene o imposta se visualizzare il numero senza un punto finale. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Ottiene o imposta il testo che si trova tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere nullo. |
| [SeparatorCharacter](../../aspose.words.fields/fieldautonumlgl/separatorcharacter) { get; set; } | Ottiene o imposta il carattere separatore da utilizzare. |
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

Inserisce un numero automatico in formato legale.

### Esempi

Mostra come organizzare un documento utilizzando i campi AUTONUMLGL.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // I campi AUTONUMLGL visualizzano un numero che aumenta ad ogni campo AUTONUMLGL all'interno del livello di intestazione corrente.
    // Questi campi mantengono un conteggio separato per ogni livello di intestazione,
     // e ogni campo visualizza anche i conteggi del campo AUTONUMLGL per tutti i livelli di intestazione al di sotto del proprio.
    // La modifica del conteggio per qualsiasi livello di intestazione reimposta i conteggi per tutti i livelli al di sopra di quel livello a 1.
    // Questo ci permette di organizzare il nostro documento sotto forma di un elenco di bozze.
    // Questo è il primo campo AUTONUMLGL a un livello di intestazione di 1, che mostra "1". nel documento.
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // Questo è il secondo campo AUTONUMLGL a livello di intestazione 1, quindi visualizzerà "2.".
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // Questo è il primo campo AUTONUMLGL a livello di intestazione 2,
    // e il conteggio AUTONUMLGL per il livello di intestazione sottostante è "2", quindi visualizzerà "2.1.".
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // Questo è il primo campo AUTONUMLGL a livello di intestazione 3.
    // Funzionando allo stesso modo del campo sopra, visualizzerà "2.1.1.".
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // Questo campo è a un livello di intestazione di 2 e il rispettivo conteggio AUTONUMLGL è a 2, quindi il campo visualizzerà "2.2.".
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // Incremento del conteggio AUTONUMLGL per un livello di intestazione inferiore a questo
    // ha azzerato il conteggio per questo livello in modo che questo campo visualizzi "2.2.1.".
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal))
    {
        // Il carattere separatore, che appare nel campo risultato subito dopo il numero,
        // è un punto fermo per impostazione predefinita. Se lasciamo questa proprietà nulla,
        // il nostro ultimo campo AUTONUMLGL visualizzerà "2.2.1." nel documento.
        Assert.IsNull(field.SeparatorCharacter);

        // Impostazione di un carattere separatore personalizzato e rimozione del punto finale
        // cambierà l'aspetto di quel campo da "2.2.1." a "2:2:1".
        // Lo applicheremo a tutti i campi che abbiamo creato.
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");

/// <summary>
/// Utilizza un generatore di documenti per inserire una clausola numerata da un campo AUTONUMLGL.
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // Questo testo apparterrà al campo legale auto num sopra di esso.
    // Si comprimerà quando si fa clic sulla freccia accanto al campo AUTONUMLGL corrispondente in Microsoft Word.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### Guarda anche

* class [Field](../field)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
