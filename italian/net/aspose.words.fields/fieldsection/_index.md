---
title: FieldSection Class
linktitle: FieldSection
articleTitle: FieldSection
second_title: Aspose.Words per .NET
description: Aspose.Words.Fields.FieldSection classe. Implementa il campo SEZIONE in C#.
type: docs
weight: 2360
url: /it/net/aspose.words.fields/fieldsection/
---
## FieldSection class

Implementa il campo SEZIONE.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldSection : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldSection](fieldsection/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene a[`FieldFormat`](../fieldformat/) oggetto che fornisce accesso digitato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non deve ricalcolare il risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere`nullo` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ottiene il tipo di campo Microsoft Word. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Restituisce il testo compreso tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice di campo che il risultato del campo dei campi secondari. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce`nullo` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Esegue l'aggiornamento del campo. Genera un risultato se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Esegue un aggiornamento del campo. Genera un risultato se il campo è già in fase di aggiornamento. |

## Osservazioni

Recupera il numero della sezione corrente.

## Esempi

Mostra come utilizzare i campi SECTION e SECTIONPAGES per numerare le pagine in sezioni.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;

// Un campo SEZIONE visualizza il numero della sezione in cui si trova.
builder.Write("Section ");
FieldSection fieldSection = (FieldSection)builder.InsertField(FieldType.FieldSection, true);

Assert.AreEqual(" SECTION ", fieldSection.GetFieldCode());

// Un campo PAGINA visualizza il numero della pagina in cui si trova.
builder.Write("\nPage ");
FieldPage fieldPage = (FieldPage)builder.InsertField(FieldType.FieldPage, true);

Assert.AreEqual(" PAGE ", fieldPage.GetFieldCode());

// Un campo SECTIONPAGES visualizza il numero di pagine su cui si estende la sezione in cui si trova.
builder.Write(" of ");
FieldSectionPages fieldSectionPages = (FieldSectionPages)builder.InsertField(FieldType.FieldSectionPages, true);

Assert.AreEqual(" SECTIONPAGES ", fieldSectionPages.GetFieldCode());

// Esci dall'intestazione e torna nel documento principale e inserisce due pagine.
// Tutte queste pagine saranno nella prima sezione. I nostri campi, che compaiono una volta in ogni intestazione,
// numererà le pagine correnti/totali di questa sezione.
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);
builder.InsertBreak(BreakType.PageBreak);

// Possiamo inserire una nuova sezione con il generatore di documenti in questo modo.
// Ciò influenzerà i valori visualizzati nei campi SECTION e SECTIONPAGES in tutte le intestazioni successive.
builder.InsertBreak(BreakType.SectionBreakNewPage);

// Il campo PAGINA continuerà a contare le pagine dell'intero documento.
// Possiamo reimpostarne manualmente il conteggio in ciascuna sezione per tenere traccia delle pagine sezione per sezione.
builder.CurrentSection.PageSetup.RestartPageNumbering = true;
builder.InsertBreak(BreakType.PageBreak);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SECTION.SECTIONPAGES.docx");
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
