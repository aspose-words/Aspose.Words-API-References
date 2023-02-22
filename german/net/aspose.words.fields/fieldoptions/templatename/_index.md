---
title: FieldOptions.TemplateName
second_title: Aspose.Words für .NET-API-Referenz
description: FieldOptions eigendom. Ruft den Dateinamen der vom Dokument verwendeten Vorlage ab oder legt ihn fest.
type: docs
weight: 170
url: /de/net/aspose.words.fields/fieldoptions/templatename/
---
## FieldOptions.TemplateName property

Ruft den Dateinamen der vom Dokument verwendeten Vorlage ab oder legt ihn fest.

```csharp
public string TemplateName { get; set; }
```

### Bemerkungen

Diese Eigenschaft wird von der verwendet[`FieldTemplate`](../../fieldtemplate/) Feld, wenn die[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) Eigentum ist leer.

Wenn diese Eigenschaft leer ist, der Standardname der Vorlagendatei`Normal.dotm` wird genutzt.

### Beispiele

Zeigt, wie ein TEMPLATE-Feld verwendet wird, um den lokalen Dateisystemspeicherort einer Dokumentvorlage anzuzeigen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wir können einen Vorlagennamen mit den Feldern festlegen. Diese Eigenschaft wird verwendet, wenn "doc.AttachedTemplate" leer ist.
// Wenn diese Eigenschaft leer ist, wird der Standard-Template-Dateiname "Normal.dotm" verwendet.
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
* namensraum [Aspose.Words.Fields](../../fieldoptions/)
* Montage [Aspose.Words](../../../)


