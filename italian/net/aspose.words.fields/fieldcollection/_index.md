---
title: FieldCollection Class
linktitle: FieldCollection
articleTitle: FieldCollection
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.FieldCollection, una potente classe per la gestione di oggetti Field all'interno di intervalli di documenti specificati, migliorando l'automazione dei tuoi documenti.
type: docs
weight: 2100
url: /it/net/aspose.words.fields/fieldcollection/
---
## FieldCollection class

Una raccolta di[`Field`](../field/) oggetti che rappresentano i campi nell'intervallo specificato.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class FieldCollection : IEnumerable<Field>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.fields/fieldcollection/count/) { get; } | Restituisce il numero di campi nella raccolta. |
| [Item](../../aspose.words.fields/fieldcollection/item/) { get; } | Restituisce un campo all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clear](../../aspose.words.fields/fieldcollection/clear/)() | Rimuove tutti i campi di questa raccolta dal documento e dalla raccolta stessa. |
| [GetEnumerator](../../aspose.words.fields/fieldcollection/getenumerator/)() | Restituisce un oggetto enumeratore. |
| [Remove](../../aspose.words.fields/fieldcollection/remove/)(*[Field](../field/)*) | Rimuove il campo specificato da questa raccolta e dal documento. |
| [RemoveAt](../../aspose.words.fields/fieldcollection/removeat/)(*int*) | Rimuove un campo all'indice specificato da questa raccolta e dal documento. |

## Osservazioni

Un'istanza di questa raccolta esegue l'iterazione dei campi che iniziano a rientrare nell'intervallo specificato.

IL`FieldCollection` la raccolta non possiede i campi che contiene, ma è semplicemente una selezione di campi.

IL`FieldCollection` la raccolta è "live", ovvero le modifiche ai figli del nodo object da cui è stata creata vengono immediatamente riflesse nei campi restituiti da`FieldCollection` Proprietà e metodi .

## Esempi

Mostra come rimuovere campi da una raccolta di campi.

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

// Di seguito sono riportati quattro modi per rimuovere campi da una raccolta di campi.
// 1 - Ottenere che un campo si rimuova da solo:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Ottenere dalla raccolta la rimozione di un campo che passiamo al suo metodo di rimozione:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Rimuovi un campo da una raccolta in corrispondenza di un indice:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Rimuovi tutti i campi dalla raccolta in una volta sola:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

Mostra come lavorare con una raccolta di campi.

```csharp
public void FieldCollection()
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

    // Esegui l'iterazione sulla raccolta dei campi e stampa il contenuto e il tipo
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
}

/// <summary>
/// Implementazione del visitatore del documento che stampa le informazioni sui campi.
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
    /// Chiamato quando nel documento viene rilevato un nodo FieldStart.
    /// </summary>
    public override VisitorAction VisitFieldStart(FieldStart fieldStart)
    {
        mBuilder.AppendLine("Found field: " + fieldStart.FieldType);
        mBuilder.AppendLine("\tField code: " + fieldStart.GetField().GetFieldCode());
        mBuilder.AppendLine("\tDisplayed as: " + fieldStart.GetField().Result);

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo FieldSeparator.
    /// </summary>
    public override VisitorAction VisitFieldSeparator(FieldSeparator fieldSeparator)
    {
        mBuilder.AppendLine("\tFound separator: " + fieldSeparator.GetText());

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Chiamato quando nel documento viene rilevato un nodo FieldEnd.
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

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
