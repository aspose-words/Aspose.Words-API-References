---
title: Document.AttachedTemplate
linktitle: AttachedTemplate
articleTitle: AttachedTemplate
second_title: Aspose.Words für .NET
description: Erfahren Sie, wie Sie die Eigenschaft „Dokument-AttachedTemplate“ effizient verwalten. Legen Sie den vollständigen Pfad Ihrer Dokumentvorlage einfach fest oder rufen Sie ihn ab, um eine nahtlose Integration zu gewährleisten.
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
| ArgumentNullException | Wirft, wenn Sie versuchen, auf eine`null` Wert. |

## Bemerkungen

Eine leere Zeichenfolge bedeutet, dass das Dokument an die normale Vorlage angehängt ist.

## Beispiele

Zeigt, wie eine Standardvorlage für Dokumente festgelegt wird, denen keine Vorlagen angehängt sind.

```csharp
Document doc = new Document();

// Automatische Stilaktualisierung aktivieren, aber kein Vorlagendokument anhängen.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Da es kein Vorlagendokument gibt, gab es im Dokument keine Möglichkeit, Stiländerungen nachzuverfolgen.
// Verwenden Sie ein SaveOptions-Objekt, um automatisch eine Vorlage festzulegen
// wenn ein Dokument, das wir speichern, keines hat.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Siehe auch

* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
