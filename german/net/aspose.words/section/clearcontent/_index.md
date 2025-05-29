---
title: Section.ClearContent
linktitle: ClearContent
articleTitle: ClearContent
second_title: Aspose.Words für .NET
description: Mit der ClearContent-Methode können Sie mühelos Abschnitte löschen. Verbessern Sie Ihren Workflow und steigern Sie die Effizienz Ihres Content-Managements!
type: docs
weight: 110
url: /de/net/aspose.words/section/clearcontent/
---
## Section.ClearContent method

Löscht den Abschnitt.

```csharp
public void ClearContent()
```

## Bemerkungen

Der Text von[`Body`](../body/) gelöscht ist, bleibt nur ein leerer Absatz übrig, der den Abschnittsumbruch darstellt.

Der Text aller Kopf- und Fußzeilen wird gelöscht, aber[`HeaderFooter`](../../headerfooter/) Objekte selbst werden nicht entfernt.

## Beispiele

Zeigt, wie der Inhalt eines Abschnitts gelöscht wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Durch Ausführen der Methode „ClearContent“ werden alle Abschnittsinhalte entfernt
//, aber lassen Sie einen leeren Absatz, um erneut Inhalt hinzuzufügen.
doc.FirstSection.ClearContent();

Assert.AreEqual(string.Empty, doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);
```

### Siehe auch

* class [Section](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
