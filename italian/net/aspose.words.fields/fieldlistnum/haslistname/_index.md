---
title: FieldListNum.HasListName
linktitle: HasListName
articleTitle: HasListName
second_title: Aspose.Words per .NET
description: FieldListNum HasListName proprietà. Restituisce un valore che indica se il nome di una definizione di numerazione astratta è fornito dal codice del campo in C#.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldlistnum/haslistname/
---
## FieldListNum.HasListName property

Restituisce un valore che indica se il nome di una definizione di numerazione astratta è fornito dal codice del campo.

```csharp
public bool HasListName { get; }
```

## Esempi

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

* class [FieldListNum](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
