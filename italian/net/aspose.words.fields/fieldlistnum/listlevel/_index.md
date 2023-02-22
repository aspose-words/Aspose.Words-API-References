---
title: FieldListNum.ListLevel
second_title: Aspose.Words per .NET API Reference
description: FieldListNum proprietà. Ottiene o imposta il livello nellelenco sovrascrivendo il comportamento predefinito del campo.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldlistnum/listlevel/
---
## FieldListNum.ListLevel property

Ottiene o imposta il livello nell'elenco, sovrascrivendo il comportamento predefinito del campo.

```csharp
public string ListLevel { get; set; }
```

### Esempi

Mostra come numerare i paragrafi con i campi LISTNUM.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// I campi LISTNUM visualizzano un numero che aumenta ad ogni campo LISTNUM.
// Questi campi hanno anche una varietà di opzioni che ci consentono di usarli per emulare elenchi numerati.
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// Gli elenchi iniziano a contare da 1 per impostazione predefinita, ma possiamo impostare questo numero su un valore diverso, ad esempio 0.
// Questo campo visualizzerà "0)".
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

 // I campi LISTNUM mantengono conteggi separati per ogni livello di elenco.
// Inserimento di un campo LISTNUM nello stesso paragrafo di un altro campo LISTNUM
// aumenta il livello dell'elenco invece del conteggio.
// Il campo successivo continuerà il conteggio iniziato in precedenza e visualizzerà un valore di "1" a livello di elenco 1.
builder.InsertField(FieldType.FieldListNum, true);

// Questo campo avvierà un conteggio a livello di elenco 2. Visualizzerà un valore di "1".
builder.InsertField(FieldType.FieldListNum, true);

// Questo campo avvierà un conteggio a livello di elenco 3. Visualizzerà un valore di "1".
// Livelli di elenco diversi hanno una formattazione diversa,
// quindi questi campi combinati visualizzeranno un valore di "1)a)i)".
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// Il prossimo campo LISTNUM che inseriamo continuerà il conteggio a livello di elenco
// che il campo LISTNUM precedente era attivo.
// Possiamo usare la proprietà "ListLevel" per passare a un livello di elenco diverso.
// Se questo campo LISTNUM rimanesse al livello di elenco 3, visualizzerebbe "ii)",
// ma, poiché l'abbiamo spostato al livello 2 della lista, continua il conteggio a quel livello e mostra "b)".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// Possiamo impostare la proprietà ListName per ottenere il campo per emulare un diverso tipo di campo AUTONUM.
// "NumberDefault" emula AUTONUM, "OutlineDefault" emula AUTONUMOUT,
// e "LegalDefault" emula i campi AUTONUMLGL.
// Il nome dell'elenco "OutlineDefault" con 1 come numero iniziale risulterà nella visualizzazione di "I.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// Il ListName non viene riportato dal campo precedente, quindi dovremo impostarlo per ogni nuovo campo.
// Questo campo continua il conteggio con il nome dell'elenco diverso e visualizza "II.".
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### Guarda anche

* class [FieldListNum](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldlistnum/)
* assemblea [Aspose.Words](../../../)


