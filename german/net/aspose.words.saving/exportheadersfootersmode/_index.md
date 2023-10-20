---
title: ExportHeadersFootersMode Enum
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words für .NET
description: Aspose.Words.Saving.ExportHeadersFootersMode opsomming. Gibt an wie Kopf und Fußzeilen nach HTML MHTML oder EPUB exportiert werden in C#.
type: docs
weight: 5000
url: /de/net/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enumeration

Gibt an, wie Kopf- und Fußzeilen nach HTML, MHTML oder EPUB exportiert werden.

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

Zeigt, wie Kopf-/Fußzeilen weggelassen werden, wenn ein Dokument im HTML-Format gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Dieses Dokument enthält Kopf- und Fußzeilen. Auf sie können wir über die Sammlung „HeadersFooters“ zugreifen.
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// Formate wie .html teilen das Dokument nicht in Seiten auf, sodass Kopf- und Fußzeilen nicht auf die gleiche Weise funktionieren
// Das würden sie tun, wenn wir das Dokument als .docx mit Microsoft Word öffnen.
// Wenn wir ein Dokument mit Kopf-/Fußzeilen in HTML konvertieren, werden bei der Konvertierung die Kopf-/Fußzeilen in den Textkörper übernommen.
// Wir können ein SaveOptions-Objekt verwenden, um beim Konvertieren in HTML Kopf-/Fußzeilen wegzulassen.
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// Öffnen Sie unser gespeichertes Dokument und stellen Sie sicher, dass es den Text der Kopfzeile nicht enthält
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### Siehe auch

* property [ExportHeadersFootersMode](../htmlsaveoptions/exportheadersfootersmode/)
* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
