---
title: FieldIncludeText
second_title: Aspose.Words per .NET API Reference
description: Implementa il campo INCLUDETEXT.
type: docs
weight: 1900
url: /it/net/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class

Implementa il campo INCLUDETEXT.

```csharp
public class FieldIncludeText : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldIncludeText](fieldincludetext)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldincludetext/bookmarkname) { get; set; } | Ottiene o imposta il nome del segnalibro nel documento da includere. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [Encoding](../../aspose.words.fields/fieldincludetext/encoding) { get; set; } | Ottiene o imposta la codifica applicata ai dati all'interno del file di riferimento. |
| [End](../../aspose.words.fields/field/end) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format) { get; } | Ottiene a[`FieldFormat`](../fieldformat) oggetto che fornisce l'accesso digitato alla formattazione del campo. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolarne il risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [LockFields](../../aspose.words.fields/fieldincludetext/lockfields) { get; set; } | Ottiene o imposta se impedire l'aggiornamento dei campi nel documento incluso. |
| [MimeType](../../aspose.words.fields/fieldincludetext/mimetype) { get; set; } | Ottiene o imposta il tipo MIME del file di riferimento. |
| [NamespaceMappings](../../aspose.words.fields/fieldincludetext/namespacemappings) { get; set; } | Ottiene o imposta i mapping dello spazio dei nomi per le query XPath. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Ottiene o imposta il testo che si trova tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere nullo. |
| [SourceFullName](../../aspose.words.fields/fieldincludetext/sourcefullname) { get; set; } | Ottiene o imposta la posizione del documento utilizzando un IRI. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| [TextConverter](../../aspose.words.fields/fieldincludetext/textconverter) { get; set; } | Ottiene o imposta il nome del convertitore di testo per il formato del file incluso. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ottiene il tipo di campo di Microsoft Word. |
| [XPath](../../aspose.words.fields/fieldincludetext/xpath) { get; set; } | Ottiene o imposta XPath per la parte desiderata del file XML. |
| [XslTransformation](../../aspose.words.fields/fieldincludetext/xsltransformation) { get; set; } | Ottiene o imposta la posizione della trasformazione XSL per formattare i dati XML. |

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

Inserisce tutto o parte del testo e della grafica contenuti in un altro documento.

### Esempi

Mostra come creare un campo INCLUDETEXT e impostarne le proprietà.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Di seguito sono riportati due modi per utilizzare i campi INCLUDETEXT per visualizzare il contenuto di un file XML nel file system locale.
    // 1 - Esegui una trasformazione XSL su un documento XML:
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 - Usa un XPath per prendere elementi specifici da un documento XML:
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");

/// <summary>
/// Utilizza un generatore di documenti per inserire un campo INCLUDETEXT con proprietà personalizzate.
/// </summary>
public FieldIncludeText CreateFieldIncludeText(DocumentBuilder builder, string sourceFullName, bool lockFields, string mimeType, string textConverter, string encoding)
{
    FieldIncludeText fieldIncludeText = (FieldIncludeText)builder.InsertField(FieldType.FieldIncludeText, true);
    fieldIncludeText.SourceFullName = sourceFullName;
    fieldIncludeText.LockFields = lockFields;
    fieldIncludeText.MimeType = mimeType;
    fieldIncludeText.TextConverter = textConverter;
    fieldIncludeText.Encoding = encoding;

    return fieldIncludeText;
}
```

### Guarda anche

* class [Field](../field)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
