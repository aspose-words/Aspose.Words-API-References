---
title: FieldTemplate.IncludeFullPath
linktitle: IncludeFullPath
articleTitle: IncludeFullPath
second_title: Aspose.Words für .NET
description: FieldTemplate IncludeFullPath eigendom. Ruft ab oder legt fest ob der vollständige Dateipfadname einbezogen werden soll in C#.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldtemplate/includefullpath/
---
## FieldTemplate.IncludeFullPath property

Ruft ab oder legt fest, ob der vollständige Dateipfadname einbezogen werden soll.

```csharp
public bool IncludeFullPath { get; set; }
```

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

* class [FieldTemplate](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
