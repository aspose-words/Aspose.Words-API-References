---
title: FieldOptions.TemplateName
linktitle: TemplateName
articleTitle: TemplateName
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FieldOptions TemplateName“, um den Vorlagendateinamen Ihres Dokuments einfach zu verwalten und so die Organisation und Effizienz zu verbessern.
type: docs
weight: 190
url: /de/net/aspose.words.fields/fieldoptions/templatename/
---
## FieldOptions.TemplateName property

Ruft den Dateinamen der vom Dokument verwendeten Vorlage ab oder legt ihn fest.

```csharp
public string TemplateName { get; set; }
```

## Bemerkungen

Diese Eigenschaft wird verwendet von[`FieldTemplate`](../../fieldtemplate/) Feld, wenn das[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) Eigenschaft ist leer.

Wenn diese Eigenschaft leer ist, wird der Standard-Vorlagendateiname`Normal.dotm` verwendet wird.

## Beispiele

Zeigt, wie Sie mithilfe eines TEMPLATE-Felds den Speicherort der Vorlage eines Dokuments im lokalen Dateisystem anzeigen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wir können einen Vorlagennamen mithilfe der Felder festlegen. Diese Eigenschaft wird verwendet, wenn "doc.AttachedTemplate" leer ist.
// Wenn diese Eigenschaft leer ist, wird der Standardvorlagendateiname „Normal.dotm“ verwendet.
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

### Siehe auch

* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
