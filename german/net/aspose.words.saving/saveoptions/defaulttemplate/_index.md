---
title: SaveOptions.DefaultTemplate
linktitle: DefaultTemplate
articleTitle: DefaultTemplate
second_title: Aspose.Words für .NET
description: Verwalten Sie Ihre SaveOptions ganz einfach! Legen Sie den Standard-Vorlagenpfad und -dateinamen fest oder erhalten Sie ihn für eine optimierte Dokumentenverarbeitung. Optimieren Sie Ihren Workflow noch heute!
type: docs
weight: 40
url: /de/net/aspose.words.saving/saveoptions/defaulttemplate/
---
## SaveOptions.DefaultTemplate property

Ruft den Pfad zur Standardvorlage ab oder legt ihn fest (einschließlich Dateiname). Der Standardwert für diese Eigenschaft ist**leere Zeichenfolge** (Empty ).

```csharp
public string DefaultTemplate { get; set; }
```

## Bemerkungen

Wenn angegeben, wird dieser Pfad zum Laden der Vorlage verwendet, wenn[`AutomaticallyUpdateStyles`](../../../aspose.words/document/automaticallyupdatestyles/) Ist`WAHR` , aber[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) ist leer.

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

* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
