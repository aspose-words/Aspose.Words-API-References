---
title: ViewOptions.DoNotDisplayPageBoundaries
linktitle: DoNotDisplayPageBoundaries
articleTitle: DoNotDisplayPageBoundaries
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die ViewOptions-Eigenschaft „DoNotDisplayPageBoundaries“ Ihr Layout verbessert, indem sie den oberen Randbereich eliminiert und so für ein saubereres, professionelleres Erscheinungsbild sorgt.
type: docs
weight: 20
url: /de/net/aspose.words.settings/viewoptions/donotdisplaypageboundaries/
---
## ViewOptions.DoNotDisplayPageBoundaries property

Deaktiviert die Anzeige des Abstands zwischen der Oberkante des Textes und dem oberen Seitenrand.

```csharp
public bool DoNotDisplayPageBoundaries { get; set; }
```

## Beispiele

Zeigt, wie vertikale Leerzeichen und Kopf-/Fußzeilen in den Ansichtsoptionen ausgeblendet werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inhalt einfügen, der sich über 3 Seiten erstreckt.
builder.Writeln("Paragraph 1, Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 2, Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Paragraph 3, Page 3.");

// Fügen Sie eine Kopf- und eine Fußzeile ein.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the footer.");

// Dieses Dokument enthält eine kleine Menge an Inhalt, der mehrere Seiten Platz einnimmt.
// Setzen Sie das Flag „DoNotDisplayPageBoundaries“ auf „true“, damit ältere Versionen von Microsoft Word Überschriften weglassen,
// Fußzeilen und ein Großteil des vertikalen Leerraums bei der Anzeige unseres Dokuments.
// Setzen Sie das Flag "DoNotDisplayPageBoundaries" auf "false", um ältere Versionen von Microsoft Word zu erhalten
// um unser Dokument normal anzuzeigen.
doc.ViewOptions.DoNotDisplayPageBoundaries = doNotDisplayPageBoundaries;

doc.Save(ArtifactsDir + "ViewOptions.DisplayPageBoundaries.doc");
```

### Siehe auch

* class [ViewOptions](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
