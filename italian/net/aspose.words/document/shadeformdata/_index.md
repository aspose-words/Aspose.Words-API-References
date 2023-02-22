---
title: Document.ShadeFormData
second_title: Aspose.Words per .NET API Reference
description: Document proprietà. Specifica se attivare lombreggiatura grigia sui campi modulo.
type: docs
weight: 360
url: /it/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

Specifica se attivare l'ombreggiatura grigia sui campi modulo.

```csharp
public bool ShadeFormData { get; set; }
```

### Esempi

Mostra come applicare l'ombreggiatura grigia ai campi modulo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// Possiamo disattivare l'ombreggiatura grigia, in modo che il testo aggiunto ai segnalibri si mescoli con l'altro testo.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


