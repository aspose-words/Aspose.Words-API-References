---
title: ExportHeadersFootersMode Enum
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words ExportHeadersFootersMode-Aufzählung für nahtlose HTML-, MHTML- oder EPUB-Kopf- und Fußzeilenexporte. Optimieren Sie noch heute Ihre Dokumentkonvertierung!
type: docs
weight: 5750
url: /de/net/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enumeration

Gibt an, wie Kopf- und Fußzeilen in HTML, MHTML oder EPUB exportiert werden.

```csharp
public enum ExportHeadersFootersMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Kopf- und Fußzeilen werden nicht exportiert. |
| PerSection | `1` | Primäre Kopf- und Fußzeilen werden am Anfang und am Ende jedes Abschnitts exportiert. |
| FirstSectionHeaderLastSectionFooter | `2` | Die primäre Kopfzeile des ersten Abschnitts wird am Anfang des Dokuments exportiert und die primäre Fußzeile befindet sich am Ende. |
| FirstPageHeaderFooterPerSection | `3` | Kopf- und Fußzeile der ersten Seite werden am Anfang und am Ende jedes Abschnitts exportiert. |

## Beispiele

Zeigt, wie Kopf-/Fußzeilen beim Speichern eines Dokuments im HTML-Format weggelassen werden.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Dieses Dokument enthält Kopf- und Fußzeilen. Wir können über die Sammlung „HeadersFooters“ darauf zugreifen.
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// Formate wie .html teilen das Dokument nicht in Seiten auf, daher funktionieren Kopf-/Fußzeilen nicht auf die gleiche Weise
// das würden sie, wenn wir das Dokument als .docx mit Microsoft Word öffnen.
// Wenn wir ein Dokument mit Kopf-/Fußzeilen in HTML konvertieren, werden die Kopf-/Fußzeilen bei der Konvertierung in den Fließtext integriert.
// Wir können ein SaveOptions-Objekt verwenden, um Kopf-/Fußzeilen beim Konvertieren in HTML wegzulassen.
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// Öffnen Sie unser gespeichertes Dokument und überprüfen Sie, ob es den Text der Kopfzeile nicht enthält
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### Siehe auch

* property [ExportHeadersFootersMode](../htmlsaveoptions/exportheadersfootersmode/)
* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
