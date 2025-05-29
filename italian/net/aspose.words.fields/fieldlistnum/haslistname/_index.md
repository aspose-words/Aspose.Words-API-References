---
title: FieldListNum.HasListName
linktitle: HasListName
articleTitle: HasListName
second_title: Aspose.Words per .NET
description: Scopri come la proprietà FieldListNum HasListName indica se un nome di definizione di numerazione astratta è incluso nel codice dei campi per una formattazione avanzata del documento.
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

// I campi LISTNUM visualizzano un numero che aumenta in ogni campo LISTNUM.
// Questi campi hanno anche una serie di opzioni che ci consentono di utilizzarli per emulare elenchi numerati.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Per impostazione predefinita, gli elenchi iniziano il conteggio da 1, ma è possibile impostare questo numero su un valore diverso, ad esempio 0.
// In questo campo verrà visualizzato "0)".
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

// I campi LISTNUM mantengono conteggi separati per ogni livello di elenco.
// Inserimento di un campo LISTNUM nello stesso paragrafo di un altro campo LISTNUM
// aumenta il livello dell'elenco anziché il conteggio.
// Il campo successivo continuerà il conteggio iniziato sopra e visualizzerà il valore "1" al livello di elenco 1.
builder.InsertField(FieldType.FieldListNum, true);

// Questo campo avvierà un conteggio a livello di elenco 2. Verrà visualizzato il valore "1".
builder.InsertField(FieldType.FieldListNum, true);

// Questo campo avvierà un conteggio dal livello 3 dell'elenco. Verrà visualizzato il valore "1".
// Diversi livelli di elenco hanno formattazioni diverse,
// quindi questi campi combinati mostreranno il valore "1)a)i)".
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Il prossimo campo LISTNUM che inseriamo continuerà il conteggio a livello di elenco
// su cui era attivo il campo LISTNUM precedente.
// Possiamo usare la proprietà "ListLevel" per passare a un livello di elenco diverso.
// Se questo campo LISTNUM rimanesse al livello di elenco 3, visualizzerebbe "ii)",
// ma, poiché lo abbiamo spostato al livello 2 dell'elenco, continua il conteggio a quel livello e visualizza "b)".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Possiamo impostare la proprietà ListName per far sì che il campo emuli un tipo di campo AUTONUM diverso.
// "NumberDefault" emula AUTONUM, "OutlineDefault" emula AUTONUMOUT,
// e "LegalDefault" emula i campi AUTONUMLGL.
// Il nome dell'elenco "OutlineDefault" con 1 come numero iniziale darà come risultato la visualizzazione di "I.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// Il campo ListName non viene trasferito dal campo precedente, quindi dovremo impostarlo per ogni nuovo campo.
// Questo campo continua il conteggio con un nome di elenco diverso e visualizza "II.".
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
