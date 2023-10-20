---
title: Document.ShadeFormData
linktitle: ShadeFormData
articleTitle: ShadeFormData
second_title: Aspose.Words per .NET
description: Document ShadeFormData proprietà. Specifica se attivare lombreggiatura grigia sui campi del modulo in C#.
type: docs
weight: 380
url: /it/net/aspose.words/document/shadeformdata/
---
## Document.ShadeFormData property

Specifica se attivare l'ombreggiatura grigia sui campi del modulo.

```csharp
public bool ShadeFormData { get; set; }
```

## Esempi

Mostra come applicare l'ombreggiatura grigia ai campi modulo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world! ");
builder.InsertTextInput("My form field", TextFormFieldType.Regular, "",
    "Text contents of form field, which are shaded in grey by default.", 0);

// Possiamo disattivare l'ombreggiatura grigia, in modo che il testo con segnalibro si confonda con l'altro testo.
doc.ShadeFormData = useGreyShading;
doc.Save(ArtifactsDir + "Document.ShadeFormData.docx");
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
