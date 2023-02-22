---
title: HtmlFixedSaveOptions.PageMargins
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlFixedSaveOptions eigendom. Gibt die Ränder um Seiten in einem HTMLDokument an. Der Randwert wird in Punkten gemessen und sollte gleich oder größer als 0 sein. Der Standardwert ist 10 Punkte.
type: docs
weight: 120
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/pagemargins/
---
## HtmlFixedSaveOptions.PageMargins property

Gibt die Ränder um Seiten in einem HTML-Dokument an. Der Randwert wird in Punkten gemessen und sollte gleich oder größer als 0 sein. Der Standardwert ist 10 Punkte.

```csharp
public double PageMargins { get; set; }
```

### Bemerkungen

Hängt vom Wert ab[`PageHorizontalAlignment`](../pagehorizontalalignment/) Eigentum:

* Definiert den oberen, unteren und linken Seitenrand, wenn der Wert istLeft .
* Definiert die oberen, unteren und rechten Seitenränder, wenn der Wert istRight .
* Definiert die oberen und unteren Seitenränder, wenn der Wert istCenter .

### Beispiele

Zeigt, wie Seitenränder angepasst werden, wenn ein Dokument in HTML gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Document.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    PageMargins = 15
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.PageMargins.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.PageMargins/styles.css");

Assert.True(Regex.Match(outDocContents,
    "[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }").Success);
```

### Siehe auch

* class [HtmlFixedSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* Montage [Aspose.Words](../../../)


