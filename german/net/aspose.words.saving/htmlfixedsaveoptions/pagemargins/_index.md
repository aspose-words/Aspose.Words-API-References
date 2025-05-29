---
title: HtmlFixedSaveOptions.PageMargins
linktitle: PageMargins
articleTitle: PageMargins
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft HtmlFixedSaveOptions PageMargins, um die Ränder Ihres HTML-Dokuments anzupassen. Legen Sie Werte in Punkten fest, um das Layout präzise zu steuern.
type: docs
weight: 130
url: /de/net/aspose.words.saving/htmlfixedsaveoptions/pagemargins/
---
## HtmlFixedSaveOptions.PageMargins property

Gibt die Ränder um Seiten in einem HTML-Dokument an. Der Randwert wird in Punkten gemessen und sollte gleich oder größer als 0 sein. Der Standardwert ist 10 Punkte.

```csharp
public double PageMargins { get; set; }
```

## Bemerkungen

Hängt vom Wert ab[`PageHorizontalAlignment`](../pagehorizontalalignment/) Eigentum:

* Definiert den oberen, unteren und linken Seitenrand, wenn der WertLeft .
* Definiert den oberen, unteren und rechten Seitenrand, wenn der WertRight .
* Definiert die oberen und unteren Seitenränder, wenn der WertCenter .

## Beispiele

Zeigt, wie Sie die Seitenränder beim Speichern eines Dokuments im HTML-Format anpassen.

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
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
