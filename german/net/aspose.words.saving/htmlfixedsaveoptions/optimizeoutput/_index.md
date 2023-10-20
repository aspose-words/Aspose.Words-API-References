---
title: HtmlFixedSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words für .NET
description: HtmlFixedSaveOptions OptimizeOutput eigendom. Flag gibt an ob es zur Optimierung der Ausgabe erforderlich ist. Wenn dieses Flag gesetzt ist werden redundante verschachtelte Leinwände und leere Leinwände entfernt auch benachbarte Glyphen mit derselben Formatierung werden verkettet. Hinweis Die Genauigkeit der Inhaltsanzeige kann beeinträchtigt werden wenn Diese Eigenschaft ist auf festgelegtWAHR . Standard istWAHR  in C#.
type: docs
weight: 100
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/
---
## HtmlFixedSaveOptions.OptimizeOutput property

Flag gibt an, ob es zur Optimierung der Ausgabe erforderlich ist. Wenn dieses Flag gesetzt ist, werden redundante verschachtelte Leinwände und leere Leinwände entfernt, auch benachbarte Glyphen mit derselben Formatierung werden verkettet. Hinweis: Die Genauigkeit der Inhaltsanzeige kann beeinträchtigt werden, wenn Diese Eigenschaft ist auf festgelegt`WAHR` . Standard ist`WAHR` .

```csharp
public override bool OptimizeOutput { get; set; }
```

## Beispiele

Zeigt, wie man ein Dokument beim Speichern in HTML vereinfacht, indem man verschiedene überflüssige Objekte entfernt.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions { OptimizeOutput = optimizeOutput };

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html", saveOptions);

// Die Größe der optimierten Version des Dokuments beträgt fast ein Drittel der Größe des nicht optimierten Dokuments.
Assert.AreEqual(optimizeOutput ? 62521 : 191770,
    new FileInfo(ArtifactsDir + "HtmlFixedSaveOptions.OptimizeGraphicsOutput.html").Length, 200);
```

### Siehe auch

* class [HtmlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
