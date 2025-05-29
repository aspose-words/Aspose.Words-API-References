---
title: Document.ShadeFormData
linktitle: ShadeFormData
articleTitle: ShadeFormData
second_title: Aspose.Words per .NET
description: Scopri come utilizzare la proprietà ShadeFormData per migliorare la visibilità del modulo con ombreggiature grigie, ottimizzando l'esperienza utente e l'accessibilità.
type: docs
weight: 400
url: /it/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

Specifica se attivare l'ombreggiatura grigia sui campi del modulo.

```csharp
public bool ShadeFormData { get; set; }
```

## Esempi

Mostra come applicare l'ombreggiatura grigia ai campi del modulo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// Possiamo disattivare la sfumatura di grigio, in modo che il testo aggiunto ai segnalibri si mescoli con il resto del testo.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
