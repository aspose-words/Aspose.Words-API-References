---
title: FieldAddressBlock Class
linktitle: FieldAddressBlock
articleTitle: FieldAddressBlock
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldAddressBlock per integrare perfettamente i campi ADDRESSBLOCK nei tuoi documenti. Migliora l'automazione dei tuoi documenti oggi stesso!
type: docs
weight: 1940
url: /it/net/aspose.words.fields/fieldaddressblock/
---
## FieldAddressBlock class

Implementa il campo ADDRESSBLOCK.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldAddressBlock : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldAddressBlock](fieldaddressblock/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [ExcludedCountryOrRegionName](../../aspose.words.fields/fieldaddressblock/excludedcountryorregionname/) { get; set; } | Ottiene o imposta il nome del paese/regione escluso. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene un[`FieldFormat`](../fieldformat/)oggetto che fornisce accesso tipizzato alla formattazione del campo. |
| [FormatAddressOnCountryOrRegion](../../aspose.words.fields/fieldaddressblock/formataddressoncountryorregion/) { get; set; } | Ottiene o imposta se formattare l'indirizzo in base al paese/regione del destinatario come definito da POST*CODE (Universal Postal Union 2006). |
| [IncludeCountryOrRegionName](../../aspose.words.fields/fieldaddressblock/includecountryorregionname/) { get; set; } | Ottiene o imposta se includere il nome del paese/regione. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [LanguageId](../../aspose.words.fields/fieldaddressblock/languageid/) { get; set; } | Ottiene o imposta l'ID della lingua utilizzata per formattare l'indirizzo. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [NameAndAddressFormat](../../aspose.words.fields/fieldaddressblock/nameandaddressformat/) { get; set; } | Ottiene o imposta il formato del nome e dell'indirizzo. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo compreso tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ottiene il tipo di campo di Microsoft Word. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). Sono inclusi sia il codice di campo che il risultato del campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è separatore). |
| [GetFieldNames](../../aspose.words.fields/fieldaddressblock/getfieldnames/)() | Restituisce una raccolta di nomi di campi di unione di posta utilizzati dal campo. |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo nodo figlio del suo nodo padre, restituisce il paragrafo padre. Se il campo è già stato rimosso, restituisce`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Esegue l'aggiornamento del campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Esegue un aggiornamento di campo. Genera un'eccezione se il campo è già in fase di aggiornamento. |

## Osservazioni

Rappresenta un blocco di indirizzi. Unblocco di indirizzi è un blocco di testo che specifica le informazioni appropriate per un indirizzo postale, nell'ordine richiesto dal paese di destinazione.

## Esempi

Mostra come ottenere i nomi dei campi di stampa unione utilizzati da un campo.

```csharp
Document doc = new Document(MyDir + "Field sample - ADDRESSBLOCK.docx");

string[] addressFieldsExpect =
{
    "Company", "First Name", "Middle Name", "Last Name", "Suffix", "Address 1", "City", "State",
    "Country or Region", "Postal Code"
};

FieldAddressBlock addressBlockField = (FieldAddressBlock) doc.Range.Fields[0];
string[] addressBlockFieldNames = addressBlockField.GetFieldNames();
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
