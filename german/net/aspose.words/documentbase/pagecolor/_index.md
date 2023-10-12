---
title: DocumentBase.PageColor
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBase eigendom. Ruft die Seitenfarbe des Dokuments ab oder legt diese fest. Diese Eigenschaft ist eine einfachere Version vonBackgroundShape .
type: docs
weight: 60
url: /de/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

Ruft die Seitenfarbe des Dokuments ab oder legt diese fest. Diese Eigenschaft ist eine einfachere Version von[`BackgroundShape`](../backgroundshape/) .

```csharp
public Color PageColor { get; set; }
```

### Bemerkungen

Diese Eigenschaft bietet eine einfache Möglichkeit, eine einfarbige Seitenfarbe für das Dokument anzugeben. Durch das Festlegen dieser Eigenschaft wird eine entsprechende erstellt und festgelegt[`BackgroundShape`](../backgroundshape/).

Wenn die Seitenfarbe nicht festgelegt ist (z. B. wenn im Dokument keine Hintergrundform vorhanden ist), wird zurückgegeben.Empty.

### Beispiele

Zeigt, wie die Hintergrundfarbe für alle Seiten eines Dokuments festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.PageColor = System.Drawing.Color.LightGray;

doc.Save(ArtifactsDir + "DocumentBase.SetPageColor.docx");
```

### Siehe auch

* class [DocumentBase](../)
* namensraum [Aspose.Words](../../documentbase/)
* Montage [Aspose.Words](../../../)


