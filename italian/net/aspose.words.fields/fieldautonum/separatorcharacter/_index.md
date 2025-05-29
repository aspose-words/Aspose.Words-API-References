---
title: FieldAutoNum.SeparatorCharacter
linktitle: SeparatorCharacter
articleTitle: SeparatorCharacter
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldAutoNum SeparatorCharacter e personalizza facilmente il carattere separatore per una formattazione dei dati migliorata e una maggiore usabilità.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldautonum/separatorcharacter/
---
## FieldAutoNum.SeparatorCharacter property

Ottiene o imposta il carattere separatore da utilizzare.

```csharp
public string SeparatorCharacter { get; set; }
```

## Esempi

Mostra come numerare i paragrafi utilizzando i campi autonum.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ogni campo AUTONUM visualizza il valore corrente di un conteggio corrente dei campi AUTONUM,
// consentendoci di numerare automaticamente gli elementi come in un elenco numerato.
// In questo campo verrà visualizzato il numero "1.".
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// Per impostazione predefinita, il carattere separatore che appare nel risultato del campo subito dopo il numero è un punto.
// Se lasciamo questa proprietà null, il nostro secondo campo AUTONUM visualizzerà "2." nel documento.
Assert.IsNull(field.SeparatorCharacter);

// Possiamo impostare questa proprietà per applicare il primo carattere della stringa come nuovo carattere separatore.
// In questo caso, il nostro campo AUTONUM visualizzerà "2:".
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### Guarda anche

* class [FieldAutoNum](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
