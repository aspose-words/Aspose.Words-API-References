---
title: Document.AttachedTemplate
second_title: Aspose.Words für .NET-API-Referenz
description: Document eigendom. Ruft den vollständigen Pfad der an das Dokument angehängten Vorlage ab oder legt ihn fest.
type: docs
weight: 20
url: /de/net/aspose.words/document/attachedtemplate/
---
## Document.AttachedTemplate property

Ruft den vollständigen Pfad der an das Dokument angehängten Vorlage ab oder legt ihn fest.

```csharp
public string AttachedTemplate { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentNullException | Wird ausgelöst, wenn Sie versuchen, einen Nullwert festzulegen. |

### Bemerkungen

Eine leere Zeichenfolge bedeutet, dass das Dokument an die normale Vorlage angehängt ist.

### Beispiele

Zeigt, wie Sie eine Standardvorlage für Dokumente festlegen, die keine angehängten Vorlagen haben.

```csharp
Document doc = new Document();

// Automatische Stilaktualisierung aktivieren, aber kein Vorlagendokument anhängen.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Da es kein Vorlagendokument gibt, konnte das Dokument Stiländerungen nirgendwo nachverfolgen.
// Verwenden Sie ein SaveOptions-Objekt, um automatisch eine Vorlage festzulegen
// wenn ein Dokument, das wir speichern, keines hat.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


