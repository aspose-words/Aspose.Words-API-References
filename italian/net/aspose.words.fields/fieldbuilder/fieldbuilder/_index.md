---
title: FieldBuilder
linktitle: FieldBuilder
articleTitle: FieldBuilder
second_title: Aspose.Words per .NET
description: FieldBuilder costruttore. Inizializza unistanza diFieldBuilder classe in C#.
type: docs
weight: 10
url: /it/net/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder constructor

Inizializza un'istanza di[`FieldBuilder`](../) classe.

```csharp
public FieldBuilder(FieldType fieldType)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| fieldType | FieldType | Il tipo di campo da costruire. |

## Esempi

Mostra come creare e inserire un campo utilizzando un generatore di campi.

```csharp
Document doc = new Document();

// Un modo conveniente per aggiungere contenuto testuale a un documento è utilizzare un generatore di documenti.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// I campi hanno il loro costruttore, che possiamo usare per costruire un codice di campo pezzo per pezzo.
// In questo caso, costruiremo un campo BARCODE che rappresenta un codice postale degli Stati Uniti,
// e poi inserirlo davanti a Run.
FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldBarcode);
fieldBuilder.AddArgument("90210");
fieldBuilder.AddSwitch("\\f", "A");
fieldBuilder.AddSwitch("\\u");

fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph.Runs[0]);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CreateWithFieldBuilder.docx");
```

### Guarda anche

* enum [FieldType](../../fieldtype/)
* class [FieldBuilder](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
