---
title: Range.NormalizeFieldTypes
linktitle: NormalizeFieldTypes
articleTitle: NormalizeFieldTypes
second_title: Aspose.Words per .NET
description: Trasforma i tipi di campo con il metodo NormalizeFieldTypes. Assicurati che FieldStart, FieldSeparator e FieldEnd siano allineati con i codici di campo specificati per una gestione dei dati ottimale.
type: docs
weight: 90
url: /it/net/aspose.words/range/normalizefieldtypes/
---
## Range.NormalizeFieldTypes method

Modifica i valori del tipo di campo[`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) Di[`FieldStart`](../../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../../aspose.words.fields/fieldend/) in questo intervallo in modo che corrispondano ai tipi di campo contenuti nei codici di campo.

```csharp
public void NormalizeFieldTypes()
```

## Osservazioni

Utilizzare questo metodo dopo le modifiche al documento che interessano i tipi di campo.

Per modificare i valori del tipo di campo nell'intero documento utilizzare[`NormalizeFieldTypes`](../../document/normalizefieldtypes/).

## Esempi

Mostra come mantenere aggiornato il tipo di un campo con il suo codice di campo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words rileva automaticamente i tipi di campo in base ai codici di campo.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// Modifica manualmente il testo non elaborato del campo, che determina il codice del campo.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];
fieldText.Text = "PAGE";

// La modifica del codice del campo ha modificato questo campo in uno di tipo diverso,
// ma le proprietà del tipo del campo visualizzano ancora il vecchio tipo.
Assert.AreEqual("PAGE", field.GetFieldCode());
Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual(FieldType.FieldDate, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.End.FieldType);

// Aggiorna queste proprietà con questo metodo per visualizzare il valore corrente.
doc.NormalizeFieldTypes();

Assert.AreEqual(FieldType.FieldPage, field.Type);
Assert.AreEqual(FieldType.FieldPage, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.End.FieldType);
```

### Guarda anche

* class [Range](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
