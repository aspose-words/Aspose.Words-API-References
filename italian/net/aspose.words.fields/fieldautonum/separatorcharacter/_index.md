---
title: FieldAutoNum.SeparatorCharacter
second_title: Aspose.Words per .NET API Reference
description: FieldAutoNum proprietà. Ottiene o imposta il carattere separatore da utilizzare.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldautonum/separatorcharacter/
---
## FieldAutoNum.SeparatorCharacter property

Ottiene o imposta il carattere separatore da utilizzare.

```csharp
public string SeparatorCharacter { get; set; }
```

### Esempi

Mostra come numerare i paragrafi utilizzando i campi numerazione automatica.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ogni campo AUTONUM visualizza il valore corrente di un conteggio parziale di campi AUTONUM,
// permettendoci di numerare automaticamente gli elementi come un elenco numerato.
// Questo campo visualizzerà un numero "1.".
FieldAutoNum field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 1.");

Assert.AreEqual(" AUTONUM ", field.GetFieldCode());

field = (FieldAutoNum)builder.InsertField(FieldType.FieldAutoNum, true);
builder.Writeln("\tParagraph 2.");

// Il carattere separatore, che appare nel risultato del campo immediatamente dopo il numero, è un punto per impostazione predefinita.
// Se lasciamo questa proprietà nulla, il nostro secondo campo AUTONUM visualizzerà "2." nel documento.
Assert.IsNull(field.SeparatorCharacter);

// Possiamo impostare questa proprietà per applicare il primo carattere della sua stringa come nuovo carattere separatore.
// In questo caso, il nostro campo AUTONUM ora visualizzerà "2:".
field.SeparatorCharacter = ":";

Assert.AreEqual(" AUTONUM  \\s :", field.GetFieldCode());

doc.Save(ArtifactsDir + "Field.AUTONUM.docx");
```

### Guarda anche

* class [FieldAutoNum](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldautonum/)
* assemblea [Aspose.Words](../../../)


