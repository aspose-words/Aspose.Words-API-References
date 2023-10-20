---
title: FieldOptions.TemplateName
linktitle: TemplateName
articleTitle: TemplateName
second_title: Aspose.Words für .NET
description: FieldOptions TemplateName eigendom. Ruft den Dateinamen der vom Dokument verwendeten Vorlage ab oder legt diesen fest in C#.
type: docs
weight: 190
url: /de/net/aspose.words.fields/fieldoptions/templatename/
---
## FieldOptions.TemplateName property

Ruft den Dateinamen der vom Dokument verwendeten Vorlage ab oder legt diesen fest.

```csharp
public string TemplateName { get; set; }
```

## Bemerkungen

Diese Eigenschaft wird von verwendet[`FieldTemplate`](../../fieldtemplate/) Feld, wenn die[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) Die Immobilie ist leer.

Wenn diese Eigenschaft leer ist, ist dies der Standardname der Vorlagendatei`Normal.dotm` wird eingesetzt.

## Beispiele

Zeigt, wie ein TEMPLATE-Feld verwendet wird, um den lokalen Dateisystemspeicherort der Vorlage eines Dokuments anzuzeigen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wir können mithilfe der Felder einen Vorlagennamen festlegen. Diese Eigenschaft wird verwendet, wenn „doc.AttachedTemplate“ leer ist.
// Wenn diese Eigenschaft leer ist, wird der Standard-Vorlagendateiname „Normal.dotm“ verwendet.
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
