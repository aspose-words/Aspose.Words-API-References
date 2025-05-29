---
title: Document.AutomaticallyUpdateStyles
linktitle: AutomaticallyUpdateStyles
articleTitle: AutomaticallyUpdateStyles
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „AutomaticallyUpdateStyles“ in MS Word sicherstellt, dass die Stile Ihres Dokuments bei jedem Öffnen mit der Vorlage synchronisiert werden, wodurch die Konsistenz verbessert wird.
type: docs
weight: 30
url: /de/net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

Ruft ein Flag ab oder legt ein Flag fest, das angibt, ob die Stile im Dokument bei jedem Öffnen des Dokuments in MS Word aktualisiert werden, um mit den Stilen in der angehängten Vorlage übereinzustimmen.

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

## Beispiele

Zeigt, wie man einem Dokument eine Vorlage anhängt.

```csharp
Document doc = new Document();

// Microsoft Word-Dokumente werden standardmäßig mit einer angehängten Vorlage namens „Normal.dotm“ geliefert.
// Es gibt keine Standardvorlage für leere Aspose.Words-Dokumente.
Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Fügen Sie eine Vorlage an und setzen Sie dann das Flag, um Stiländerungen anzuwenden
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
