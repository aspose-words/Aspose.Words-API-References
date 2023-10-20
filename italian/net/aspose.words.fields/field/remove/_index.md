---
title: Field.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words per .NET
description: Field Remove metodo. Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è lultimo figlio del suo nodo genitore restituisce il paragrafo genitore. Se il campo è già stato rimosso restituiscenullo  in C#.
type: docs
weight: 120
url: /it/net/aspose.words.fields/field/remove/
---
## Field.Remove method

Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo genitore, restituisce il paragrafo genitore. Se il campo è già stato rimosso, restituisce`nullo` .

```csharp
public Node Remove()
```

## Esempi

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
// 1 - Ottieni un campo per rimuoversi:
fields[0].Remove();
Assert.AreEqual(5, fields.Count);

// 2 - Ottieni la raccolta per rimuovere un campo che passiamo al suo metodo di rimozione:
Field lastField = fields[3];
fields.Remove(lastField);
Assert.AreEqual(4, fields.Count);

// 3 - Rimuove un campo da una raccolta in un indice:
fields.RemoveAt(2);
Assert.AreEqual(3, fields.Count);

// 4 - Rimuovi tutti i campi dalla raccolta contemporaneamente:
fields.Clear();
Assert.AreEqual(0, fields.Count);
```

Mostra come elaborare i campi PRIVATE.

```csharp
public void FieldPrivate()
{
    // Apre un documento Corel WordPerfect che abbiamo convertito nel formato .docx.
    Document doc = new Document(MyDir + "Field sample - PRIVATE.docx");

    // I documenti WordPerfect 5.x/6.x come quello che abbiamo caricato possono contenere campi PRIVATE.
    // Microsoft Word preserva i campi PRIVATE durante le operazioni di caricamento/salvataggio,
    // ma non fornisce loro alcuna funzionalità.
    FieldPrivate field = (FieldPrivate)doc.Range.Fields[0];

    Assert.AreEqual(" PRIVATE \"My value\" ", field.GetFieldCode());
    Assert.AreEqual(FieldType.FieldPrivate, field.Type);

    // Possiamo anche inserire campi PRIVATE utilizzando un generatore di documenti.
    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.InsertField(FieldType.FieldPrivate, true);

    // Questi campi non rappresentano un modo praticabile per proteggere le informazioni sensibili.
    // A meno che la compatibilità con le versioni precedenti di WordPerfect non sia essenziale,
    // possiamo rimuovere questi campi in tutta sicurezza. Possiamo farlo utilizzando un'implementazione di DocumentVisiitor.
    Assert.AreEqual(2, doc.Range.Fields.Count);

    FieldPrivateRemover remover = new FieldPrivateRemover();
    doc.Accept(remover);

    Assert.AreEqual(2, remover.GetFieldsRemovedCount());
    Assert.AreEqual(0, doc.Range.Fields.Count);
}

/// <summary>
/// Rimuove tutti i campi PRIVATE incontrati.
/// </summary>
public class FieldPrivateRemover : DocumentVisitor
{
    public FieldPrivateRemover()
    {
        mFieldsRemovedCount = 0;
    }

    public int GetFieldsRemovedCount()
    {
        return mFieldsRemovedCount;
    }

    /// <summary>
    /// Chiamato quando nel documento viene incontrato un nodo FieldEnd.
    /// Se il nodo appartiene ad un campo PRIVATE, l'intero campo viene rimosso.
    /// </summary>
    public override VisitorAction VisitFieldEnd(FieldEnd fieldEnd)
    {
        if (fieldEnd.FieldType == FieldType.FieldPrivate)
        {
            fieldEnd.GetField().Remove();
            mFieldsRemovedCount++;
        }

        return VisitorAction.Continue;
    }

    private int mFieldsRemovedCount;
}
```

### Guarda anche

* class [Node](../../../aspose.words/node/)
* class [Field](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
