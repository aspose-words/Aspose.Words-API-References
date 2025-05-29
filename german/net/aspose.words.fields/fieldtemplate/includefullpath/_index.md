---
title: FieldTemplate.IncludeFullPath
linktitle: IncludeFullPath
articleTitle: IncludeFullPath
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldTemplate-Eigenschaft „IncludeFullPath“, um die Einbeziehung vollständiger Dateipfade einfach zu verwalten und so die Effizienz und Organisation Ihres Projekts zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldtemplate/includefullpath/
---
## FieldTemplate.IncludeFullPath property

Ruft ab oder legt fest, ob der vollständige Dateipfadname eingeschlossen werden soll.

```csharp
public bool IncludeFullPath { get; set; }
```

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

* class [FieldTemplate](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
