---
title: Enum ExportHeadersFootersMode
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.ExportHeadersFootersMode opsomming. Gibt an wie Kopf und Fußzeilen in HTML MHTML oder EPUB exportiert werden.
type: docs
weight: 4740
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

### Beispiele

Zeigt, wie Kopf-/Fußzeilen weggelassen werden, wenn ein Dokument in HTML gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Dieses Dokument enthält Kopf- und Fußzeilen. Wir können auf sie über die Sammlung "HeadersFooters" zugreifen.
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// Formate wie .html teilen das Dokument nicht in Seiten auf, daher funktionieren Kopf-/Fußzeilen nicht auf die gleiche Weise
// würden sie, wenn wir das Dokument als .docx mit Microsoft Word öffnen.
// Wenn wir ein Dokument mit Kopf-/Fußzeilen in HTML umwandeln, wird die Konvertierung die Kopf-/Fußzeilen in den Haupttext integrieren.
// Wir können ein SaveOptions-Objekt verwenden, um Kopf-/Fußzeilen beim Konvertieren in HTML wegzulassen.
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// Öffnen Sie unser gespeichertes Dokument und vergewissern Sie sich, dass es den Text der Kopfzeile nicht enthält
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### Siehe auch

* property [ExportHeadersFootersMode](../htmlsaveoptions/exportheadersfootersmode/)
* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


