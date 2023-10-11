---
title: Document.AutomaticallyUpdateStyles
second_title: Aspose.Words für .NET-API-Referenz
description: Document eigendom. Ruft ein Flag ab oder legt es fest das angibt ob die Stile im Dokument bei jedem Öffnen des Dokuments in MS Word so aktualisiert werden dass sie mit den Stilen in der angehängten Vorlage übereinstimmen.
type: docs
weight: 30
url: /de/net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

Ruft ein Flag ab oder legt es fest, das angibt, ob die Stile im Dokument bei jedem Öffnen des Dokuments in MS Word so aktualisiert werden, dass sie mit den Stilen in der angehängten Vorlage übereinstimmen.

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

### Beispiele

Zeigt, wie eine Vorlage an ein Dokument angehängt wird.

```csharp
Document doc = new Document();

// Microsoft Word-Dokumente verfügen standardmäßig über eine angehängte Vorlage namens „Normal.dotm“.
// Es gibt keine Standardvorlage für leere Aspose.Words-Dokumente.
Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Eine Vorlage anhängen und dann das Flag setzen, um Stiländerungen anzuwenden
// innerhalb der Vorlage zu Stilen in unserem Dokument.
doc.AttachedTemplate = MyDir + "Business brochure.dotx";
doc.AutomaticallyUpdateStyles = true;

doc.Save(ArtifactsDir + "Document.AutomaticallyUpdateStyles.docx");
```

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
* namensraum [Aspose.Words](../../document/)
* Montage [Aspose.Words](../../../)


