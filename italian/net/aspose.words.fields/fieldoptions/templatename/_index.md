---
title: FieldOptions.TemplateName
linktitle: TemplateName
articleTitle: TemplateName
second_title: Aspose.Words per .NET
description: Scopri la proprietà TemplateName di FieldOptions per gestire facilmente il nome del file modello del tuo documento, migliorando l'organizzazione e l'efficienza.
type: docs
weight: 190
url: /it/net/aspose.words.fields/fieldoptions/templatename/
---
## FieldOptions.TemplateName property

Ottiene o imposta il nome del file del modello utilizzato dal documento.

```csharp
public string TemplateName { get; set; }
```

## Osservazioni

Questa proprietà è utilizzata da[`FieldTemplate`](../../fieldtemplate/) campo se il[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) la proprietà è vuota.

Se questa proprietà è vuota, il nome del file modello predefinito`Normal.dotm` viene utilizzato.

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

* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
