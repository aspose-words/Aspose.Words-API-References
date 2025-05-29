---
title: FieldTemplate.IncludeFullPath
linktitle: IncludeFullPath
articleTitle: IncludeFullPath
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldTemplate IncludeFullPath per gestire facilmente l'inclusione del percorso completo dei file, migliorando l'efficienza e l'organizzazione del tuo progetto.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldtemplate/includefullpath/
---
## FieldTemplate.IncludeFullPath property

Ottiene o imposta se includere il nome completo del percorso del file.

```csharp
public bool IncludeFullPath { get; set; }
```

## Esempi

Mostra come utilizzare un campo TEMPLATE per visualizzare il percorso del file system locale del modello di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Possiamo impostare un nome per il modello utilizzando i campi. Questa proprietà viene utilizzata quando "doc.AttachedTemplate" è vuoto.
// Se questa proprietà è vuota, verrà utilizzato il nome predefinito del file modello "Normal.dotm".
doc.FieldOptions.TemplateName = string.Empty;

FieldTemplate field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
Assert.AreEqual(" TEMPLATE ", field.GetFieldCode());

builder.Writeln();
field = (FieldTemplate)builder.InsertField(FieldType.FieldTemplate, false);
field.IncludeFullPath = true;

Assert.AreEqual(" TEMPLATE  \\p", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TEMPLATE.docx");
```

### Guarda anche

* class [FieldTemplate](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
