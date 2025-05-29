---
title: DocumentBase.PageColor
linktitle: PageColor
articleTitle: PageColor
second_title: Aspose.Words für .NET
description: Entdecken Sie die DocumentBase PageColor-Eigenschaft, um die Seitenfarbe Ihres Dokuments einfach anzupassen. Vereinfachen Sie das Design mit dieser benutzerfreundlichen Funktion!
type: docs
weight: 70
url: /de/net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

Ruft die Seitenfarbe des Dokuments ab oder legt sie fest. Diese Eigenschaft ist eine einfachere Version von[`BackgroundShape`](../backgroundshape/) .

```csharp
public Color PageColor { get; set; }
```

## Bemerkungen

Diese Eigenschaft bietet eine einfache Möglichkeit, eine einheitliche Seitenfarbe für das Dokument festzulegen. Durch das Festlegen dieser Eigenschaft wird eine entsprechende[`BackgroundShape`](../backgroundshape/).

Wenn die Seitenfarbe nicht festgelegt ist (z. B. wenn im Dokument keine Hintergrundform vorhanden ist), wird zurückgegeben.Empty.

## Beispiele

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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
