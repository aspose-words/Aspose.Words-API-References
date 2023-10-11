---
title: HtmlSaveOptions.ExportHeadersFootersMode
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlSaveOptions eigendom. Gibt an wie Kopf und Fußzeilen in HTML MHTML oder EPUB ausgegeben werden. Der Standardwert istPerSection für HTML/MHTML undNone für EPUB.
type: docs
weight: 160
url: /de/net/aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/
---
## HtmlSaveOptions.ExportHeadersFootersMode property

Gibt an, wie Kopf- und Fußzeilen in HTML, MHTML oder EPUB ausgegeben werden. Der Standardwert istPerSection für HTML/MHTML undNone für EPUB.

```csharp
public ExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

### Bemerkungen

Es ist schwierig, Kopf- und Fußzeilen sinnvoll in HTML auszugeben, da HTML nicht paginiert ist.

Wenn diese Eigenschaft istPerSection, Aspose.Words exports nur primäre Kopf- und Fußzeilen am Anfang und am Ende jedes Abschnitts.

Wann ist esFirstSectionHeaderLastSectionFooter Es werden nur die erste primäre Kopfzeile und die letzte primäre Fußzeile (einschließlich der Verknüpfung mit der vorherigen) exportiert.

Sie können den Export von Kopf- und Fußzeilen vollständig deaktivieren, indem Sie diese Eigenschaft auf setzenNone.

### Beispiele

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

* enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlsaveoptions/)
* Montage [Aspose.Words](../../../)


