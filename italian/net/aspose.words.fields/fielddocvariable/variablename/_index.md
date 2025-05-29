---
title: FieldDocVariable.VariableName
linktitle: VariableName
articleTitle: VariableName
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldDocVariable VariableName per gestire facilmente le variabili dei documenti. Semplifica il recupero e migliora la gestione dei tuoi documenti oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words.fields/fielddocvariable/variablename/
---
## FieldDocVariable.VariableName property

Ottiene o imposta il nome della variabile del documento da recuperare.

```csharp
public string VariableName { get; set; }
```

## Esempi

Mostra come utilizzare i campi DOCPROPERTY per visualizzare le proprietà e le variabili del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Di seguito sono riportati due modi per utilizzare i campi DOCPROPERTY.
// 1 - Visualizza una proprietà incorporata:
// Imposta un valore personalizzato per la proprietà integrata "Categoria", quindi inserisci un campo DOCPROPERTY che vi faccia riferimento.
doc.BuiltInDocumentProperties.Category = "My category";

FieldDocProperty fieldDocProperty = (FieldDocProperty)builder.InsertField(" DOCPROPERTY Category ");
fieldDocProperty.Update();

Assert.AreEqual(" DOCPROPERTY Category ", fieldDocProperty.GetFieldCode());
Assert.AreEqual("My category", fieldDocProperty.Result);

builder.InsertParagraph();

// 2 - Visualizza una variabile di documento personalizzata:
// Definisci una variabile personalizzata, quindi fai riferimento a tale variabile con un campo DOCPROPERTY.
Assert.AreEqual(0, doc.Variables.Count);
doc.Variables.Add("My variable", "My variable's value");

FieldDocVariable fieldDocVariable = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
fieldDocVariable.VariableName = "My Variable";
fieldDocVariable.Update();

Assert.AreEqual(" DOCVARIABLE  \"My Variable\"", fieldDocVariable.GetFieldCode());
Assert.AreEqual("My variable's value", fieldDocVariable.Result);

doc.Save(ArtifactsDir + "Field.DOCPROPERTY.DOCVARIABLE.docx");
```

### Guarda anche

* class [FieldDocVariable](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
