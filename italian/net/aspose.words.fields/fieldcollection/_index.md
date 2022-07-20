---
title: FieldCollection
second_title: Aspose.Words per .NET API Reference
description: Una raccolta diField./field oggetti che rappresentano i campi nellintervallo specificato.
type: docs
weight: 1540
url: /it/net/aspose.words.fields/fieldcollection/
---
## FieldCollection class

Una raccolta di[`Field`](../field) oggetti che rappresentano i campi nell'intervallo specificato.

```csharp
public class FieldCollection : IEnumerable<Field>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.fields/fieldcollection/count) { get; } | Restituisce il numero dei campi nella raccolta. |
| [Item](../../aspose.words.fields/fieldcollection/item) { get; } | Restituisce un campo all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clear](../../aspose.words.fields/fieldcollection/clear)() | Rimuove tutti i campi di questa raccolta dal documento e da questa raccolta stessa. |
| [GetEnumerator](../../aspose.words.fields/fieldcollection/getenumerator)() | Restituisce un oggetto enumeratore. |
| [Remove](../../aspose.words.fields/fieldcollection/remove)(Field) | Rimuove il campo specificato da questa raccolta e dal documento. |
| [RemoveAt](../../aspose.words.fields/fieldcollection/removeat)(int) | Rimuove un campo in corrispondenza dell'indice specificato da questa raccolta e dal documento. |

### Osservazioni

Un'istanza di questa raccolta itera i campi che iniziano all'interno dell'intervallo specificato.

Il[`FieldCollection`](../fieldcollection) raccolta non possiede i campi che contiene, piuttosto, è solo una selezione di campi.

Il[`FieldCollection`](../fieldcollection) raccolta è "live", cioè le modifiche ai figli del nodo object da cui è stata creata si riflettono immediatamente nei campi restituiti dal[`FieldCollection`](../fieldcollection) proprietà e metodi.

### Esempi

Mostra come rimuovere i campi da una raccolta di campi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder.InsertField(" TIME ");
builder.InsertField(" REVNUM ");
builder.InsertField(" AUTHOR  \"John Doe\" ");
builder.InsertField(" SUBJECT \"My Subject\" ");
builder.InsertField(" QUOTE \"Hello world!\" ");
doc.UpdateFields();

FieldCollection fields = doc.Range.Fields;

Assert.AreEqual(6, fields.Count);

// Di seguito sono riportati quattro modi per rimuovere i campi da una raccolta di campi.
// 1 - Ottieni un campo da rimuovere:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Ottieni la raccolta per rimuovere un campo che passiamo al suo metodo di rimozione:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Rimuove un campo da una raccolta in un indice:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Rimuovi tutti i campi dalla raccolta in una volta:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

Mostra come lavorare con una raccolta di campi.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder.InsertField(" TIME ");
    builder.InsertField(" REVNUM ");
    builder.InsertField(" AUTHOR  \"John Doe\" ");
    builder.InsertField(" SUBJECT \"My Subject\" ");
    builder.InsertField(" QUOTE \"Hello world!\" ");
    doc.UpdateFields();

    FieldCollection fields = doc.Range.Fields;

    Assert.AreEqual(6, fields.Count);

    // Esegui l'iterazione sulla raccolta di campi e stampa il contenuto e il tipo
    // di ogni campo utilizzando un'implementazione personalizzata del visitatore.
    FieldVisitor fieldVisitor = new FieldVisitor();

    using (IEnumerator<Field> fieldEnumerator = fields.GetEnumerator())
    {
        while (fieldEnumerator.MoveNext())
        {
            if (fieldEnumerator.Current != null)
            {
                fieldEnumerator.Current.Start.Accept(fieldVisitor);
                fieldEnumerator.Current.Separator?.Accept(fieldVisitor);
                fieldEnumerator.Current.End.Accept(fieldVisitor);
            }
            else
            {
                Console.WriteLine("There are no fields in the document.");
            }
        }
    }

    Console.WriteLine(fieldVisitor.GetText());

/// <summary>
/// Documenta l'implementazione del visitatore che stampa le informazioni sul campo.
/// </summary>
public class FieldVisitor : DocumentVisitor
{
    public FieldVisitor()
    {
        mBuilder = new StringBuilder();
    }

    /// <summary>
    /// Ottiene il testo normale del documento accumulato dal visitatore.
    /// </summary>
    public string GetText()
    {
        return mBuilder.ToString();
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo FieldStart nel documento.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo FieldSeparator nel documento.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando viene rilevato un nodo FieldEnd nel documento.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        mBuilder.AppendLine("End of field: " + fieldEnd.FieldType);

        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### Guarda anche

* class [Field](../field)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
