---
title: Document.AttachedTemplate
linktitle: AttachedTemplate
articleTitle: AttachedTemplate
second_title: Aspose.Words für .NET
description: Document AttachedTemplate eigendom. Ruft den vollständigen Pfad der an das Dokument angehängten Vorlage ab oder legt diesen fest in C#.
type: docs
weight: 20
url: /de/net/aspose.words/document/attachedtemplate/
---
## Document.AttachedTemplate property

Ruft den vollständigen Pfad der an das Dokument angehängten Vorlage ab oder legt diesen fest.

```csharp
public string AttachedTemplate { get; set; }
```

### Ausnahmen

| Ausnahme | Bedingung |
| --- | --- |
| ArgumentNullException | Wird ausgelöst, wenn Sie versuchen, auf a zu setzen`Null` Wert. |

## Bemerkungen

Eine leere Zeichenfolge bedeutet, dass das Dokument an die Vorlage „Normal“ angehängt ist.

## Beispiele

Zeigt, wie eine Standardvorlage für Dokumente festgelegt wird, denen keine Vorlagen angehängt sind.

```csharp
Document doc = new Document();

// Automatische Stilaktualisierung aktivieren, aber kein Vorlagendokument anhängen.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Da es kein Vorlagendokument gibt, konnte das Dokument Stiländerungen nicht nachverfolgen.
// Verwenden Sie ein SaveOptions-Objekt, um automatisch eine Vorlage festzulegen
// wenn ein Dokument, das wir speichern, keins hat.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
