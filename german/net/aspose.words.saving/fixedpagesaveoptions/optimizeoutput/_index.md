---
title: FixedPageSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumentausgabe mit der OptimizeOutput-Eigenschaft von FixedPageSaveOptions. Entfernen Sie Redundanzen und verbessern Sie die Formatierung für eine übersichtlichere Darstellung.
type: docs
weight: 50
url: /de/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

Flag gibt an, ob es zur Optimierung der Ausgabe erforderlich ist. Wenn dieses Flag gesetzt ist, werden redundante verschachtelte Leinwände und leere Leinwände entfernt, auch benachbarte Glyphen mit der gleichen Formatierung werden verkettet. Hinweis: Die Genauigkeit der Inhaltsanzeige kann beeinträchtigt werden, wenn diese Eigenschaft auf`WAHR` . Standard ist`FALSCH` .

```csharp
public virtual bool OptimizeOutput { get; set; }
```

## Beispiele

Zeigt, wie Dokumentobjekte beim Speichern im XPS-Format optimiert werden.

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// Erstellen Sie ein "XpsSaveOptions"-Objekt, das an die "Save"-Methode des Dokuments übergeben wird
// um zu ändern, wie diese Methode das Dokument in .XPS konvertiert.
XpsSaveOptions saveOptions = new XpsSaveOptions();
// Setzen Sie die Eigenschaft „OptimizeOutput“ auf „true“, um Maßnahmen wie das Entfernen verschachtelter oder leerer Canvases zu ergreifen
// und Verketten benachbarter Läufe mit identischer Formatierung, um den Inhalt des Ausgabedokuments zu optimieren.
// Dies kann das Erscheinungsbild des Dokuments beeinträchtigen.
// Setzen Sie die Eigenschaft „OptimizeOutput“ auf „false“, um das Dokument normal zu speichern.
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### Siehe auch

* class [FixedPageSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
