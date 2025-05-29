---
title: HtmlFixedSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre HTML-Ausgabe mit der Eigenschaft „HtmlFixedSaveOptions“. Verbessern Sie die Leistung, indem Sie redundante Leinwände entfernen und ähnliche Glyphen zusammenführen. Standardmäßig „true“.
type: docs
weight: 110
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/
---
## HtmlFixedSaveOptions.OptimizeOutput property

Flag gibt an, ob es zur Optimierung der Ausgabe erforderlich ist. Wenn dieses Flag gesetzt ist, werden redundante verschachtelte Leinwände und leere Leinwände entfernt, auch benachbarte Glyphen mit der gleichen Formatierung werden verkettet. Hinweis: Die Genauigkeit der Inhaltsanzeige kann beeinträchtigt werden, wenn diese Eigenschaft auf`WAHR` . Standard ist`WAHR` .

```csharp
public override bool OptimizeOutput { get; set; }
```

## Beispiele

Zeigt, wie Sie ein Dokument beim Speichern im HTML-Format durch das Entfernen verschiedener redundanter Objekte vereinfachen können.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { OptimizeOutput = optimizeOutput };

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

// Die Größe der optimierten Version des Dokuments beträgt fast ein Drittel der Größe des nicht optimierten Dokuments.
Assert.AreEqual(optimizeOutput ? 60385 : 191000,
    new FileInfo(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").Length, 200);
```

### Siehe auch

* class [HtmlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
