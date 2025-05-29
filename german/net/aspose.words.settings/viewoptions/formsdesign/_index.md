---
title: ViewOptions.FormsDesign
linktitle: FormsDesign
articleTitle: FormsDesign
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie ViewOptions FormsDesign Ihr Dokumenterlebnis verbessert, indem es den Formularentwurfsmodus für nahtloses Bearbeiten und Anpassen umschaltet.
type: docs
weight: 30
url: /de/net/aspose.words.settings/viewoptions/formsdesign/
---
## ViewOptions.FormsDesign property

Gibt an, ob sich das Dokument im Formularentwurfsmodus befindet.

```csharp
public bool FormsDesign { get; set; }
```

## Bemerkungen

Funktioniert derzeit nur für Dokumente im WordML-Format.

## Beispiele

Zeigt, wie der Formularentwurfsmodus aktiviert/deaktiviert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Setzen Sie die Eigenschaft „FormsDesign“ auf „false“, um den Formularentwurfsmodus deaktiviert zu lassen.
// Setzen Sie die Eigenschaft „FormsDesign“ auf „true“, um den Formularentwurfsmodus zu aktivieren.
doc.ViewOptions.FormsDesign = useFormsDesign;

doc.Save(ArtifactsDir + "ViewOptions.FormsDesign.xml");

Assert.AreEqual(useFormsDesign,
    File.ReadAllText(ArtifactsDir + "ViewOptions.FormsDesign.xml").Contains("<w:formsDesign />"));
```

### Siehe auch

* class [ViewOptions](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
