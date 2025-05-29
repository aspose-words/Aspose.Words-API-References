---
title: ViewOptions.ViewType
linktitle: ViewType
articleTitle: ViewType
second_title: Aspose.Words für .NET
description: Entdecken Sie die ViewOptions ViewType-Eigenschaft, um Ihren Microsoft Word-Ansichtsmodus einfach anzupassen und so die Produktivität zu steigern und ein maßgeschneidertes Bearbeitungserlebnis zu ermöglichen.
type: docs
weight: 40
url: /de/net/aspose.words.settings/viewoptions/viewtype/
---
## ViewOptions.ViewType property

Steuert den Ansichtsmodus in Microsoft Word.

```csharp
public ViewType ViewType { get; set; }
```

## Bemerkungen

Obwohl Aspose.Words diese Option lesen und schreiben kann, ist ihre Verwendung anwendungsspezifisch. Beispielsweise respektiert MS Word 2013 den Wert dieser Option nicht.

## Beispiele

Zeigt, wie ein benutzerdefinierter Zoomfaktor festgelegt wird, den ältere Versionen von Microsoft Word beim Laden eines Dokuments anwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.ViewOptions.ViewType = ViewType.PageLayout;
doc.ViewOptions.ZoomPercent = 50;

Assert.AreEqual(ZoomType.Custom, doc.ViewOptions.ZoomType);
Assert.AreEqual(ZoomType.None, doc.ViewOptions.ZoomType);

doc.Save(ArtifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

### Siehe auch

* enum [ViewType](../../viewtype/)
* class [ViewOptions](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
