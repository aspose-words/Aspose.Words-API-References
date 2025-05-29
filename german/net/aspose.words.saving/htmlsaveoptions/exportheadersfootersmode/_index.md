---
title: HtmlSaveOptions.ExportHeadersFootersMode
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft HtmlSaveOptions ExportHeadersFootersMode die Kopf- und Fußzeilenausgabe für HTML-, MHTML- und EPUB-Formate optimiert. Optimieren Sie die Präsentation Ihres Dokuments!
type: docs
weight: 160
url: /de/net/aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/
---
## HtmlSaveOptions.ExportHeadersFootersMode property

Gibt an, wie Kopf- und Fußzeilen in HTML, MHTML oder EPUB ausgegeben werden. Der Standardwert istPerSection für HTML/MHTML undNone für EPUB.

```csharp
public ExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

## Bemerkungen

Es ist schwierig, Kopf- und Fußzeilen sinnvoll in HTML auszugeben, da HTML nicht paginiert ist.

Wenn diese EigenschaftPerSection, Aspose.Words exportiert nur primäre Kopf- und Fußzeilen am Anfang und am Ende jedes Abschnitts.

Wenn esFirstSectionHeaderLastSectionFooter Es werden nur die erste primäre Kopfzeile und die letzte primäre Fußzeile (einschließlich der mit der vorherigen verknüpften) exportiert.

Sie können den Export von Kopf- und Fußzeilen ganz deaktivieren, indem Sie diese Eigenschaft aufNone.

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

* enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
