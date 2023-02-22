---
title: Document.AutomaticallyUpdateStyles
second_title: Aspose.Words für .NET-API-Referenz
description: Document eigendom. Ruft ein Flag ab oder setzt es das angibt ob die Stile im Dokument jedes Mal aktualisiert werden damit sie mit den Stilen in der angehängten Vorlage übereinstimmen wenn das Dokument in MS Word geöffnet wird.
type: docs
weight: 30
url: /de/net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

Ruft ein Flag ab oder setzt es, das angibt, ob die Stile im Dokument jedes Mal aktualisiert werden, damit sie mit den Stilen in der angehängten -Vorlage übereinstimmen, wenn das Dokument in MS Word geöffnet wird.

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

### Beispiele

Zeigt, wie Sie eine Vorlage an ein Dokument anhängen.

```csharp
Document doc = new Document();

// Microsoft Word-Dokumente werden standardmäßig mit einer angehängten Vorlage namens "Normal.dotm" geliefert.
// Es gibt keine Standardvorlage für leere Aspose.Words-Dokumente.
Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Hängen Sie eine Vorlage an und setzen Sie dann das Flag, um Stiländerungen anzuwenden
// innerhalb der Vorlage zu Stilen in unserem Dokument.
doc.AttachedTemplate = MyDir + "Business brochure.dotx";
doc.AutomaticallyUpdateStyles = true;

doc.Save(ArtifactsDir + "Document.AutomaticallyUpdateStyles.docx");
```

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


