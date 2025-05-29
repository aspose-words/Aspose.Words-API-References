---
title: FieldBuilder
linktitle: FieldBuilder
articleTitle: FieldBuilder
second_title: Aspose.Words per .NET
description: Scopri FieldBuilder, il potente strumento per creare e gestire facilmente i campi nei tuoi progetti. Semplifica il tuo flusso di lavoro oggi stesso!
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

// Un modo comodo per aggiungere contenuto di testo a un documento è utilizzare un generatore di documenti.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// I campi hanno il loro costruttore, che possiamo utilizzare per costruire un codice di campo pezzo per pezzo.
// In questo caso, costruiremo un campo BARCODE che rappresenta un codice postale degli Stati Uniti,
// e quindi inserirlo davanti a Run.
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
