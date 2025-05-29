---
title: HtmlLoadOptions.WebRequestTimeout
linktitle: WebRequestTimeout
articleTitle: WebRequestTimeout
second_title: Aspose.Words für .NET
description: Entdecken Sie die WebRequestTimeout-Eigenschaft von HtmlLoadOptions, mit der Sie Timeout-Einstellungen für optimale Web-Performance anpassen können. Standardmäßig 100 Sekunden.
type: docs
weight: 80
url: /de/net/aspose.words.loading/htmlloadoptions/webrequesttimeout/
---
## HtmlLoadOptions.WebRequestTimeout property

Die Anzahl der Millisekunden, die gewartet werden soll, bevor die Webanforderung abläuft. Der Standardwert beträgt 100.000 Millisekunden (100 Sekunden).

```csharp
public int WebRequestTimeout { get; set; }
```

## Bemerkungen

Die Anzahl der Millisekunden, die Aspose.Words auf eine Antwort wartet, wenn externe Ressourcen (Bilder, Style ) geladen werden, die in HTML- und MHTML-Dokumenten verknüpft sind.

## Beispiele

Zeigt, wie Sie beim Laden eines Dokuments mit externen Ressourcen, die über URLs verknüpft sind, ein Zeitlimit für Webanforderungen festlegen.

```csharp
public void WebRequestTimeout()
{
    // Erstellen Sie ein neues HtmlLoadOptions-Objekt und überprüfen Sie seinen Timeout-Schwellenwert für eine Webanforderung.
    HtmlLoadOptions options = new HtmlLoadOptions();

    // Beim Laden eines HTML-Dokuments mit Ressourcen, die extern über eine Webadressen-URL verknüpft sind,
    // Aspose.Words bricht Webanforderungen ab, bei denen das Abrufen der Ressourcen innerhalb dieses Zeitlimits (in Millisekunden) fehlschlägt.
    Assert.AreEqual(100000, options.WebRequestTimeout);

    // Legen Sie einen WarningCallback fest, der alle Warnungen aufzeichnet, die während des Ladens auftreten.
    ListDocumentWarnings warningCallback = new ListDocumentWarnings();
    options.WarningCallback = warningCallback;

    // Laden Sie ein solches Dokument und überprüfen Sie, ob eine Form mit Bilddaten erstellt wurde.
    // Zum Laden dieses verknüpften Bildes ist eine Webanforderung erforderlich, die innerhalb unseres Zeitlimits abgeschlossen sein muss.
    string html = $@"
        <html>
            <img src=""{ImageUrl}"" alt=""Aspose logo"" style=""width:400px;height:400px;"">
        </html>
    ";

    // Legen Sie ein unangemessenes Zeitlimit fest und versuchen Sie, das Dokument erneut zu laden.
    options.WebRequestTimeout = 0;
    Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), options);
    Assert.AreEqual(2, warningCallback.Warnings().Count);

    // Eine Webanforderung, bei der innerhalb des Zeitlimits kein Bild abgerufen werden kann, erzeugt dennoch ein Bild.
    // Allerdings wird das Bild mit dem roten „x“ gekennzeichnet, das normalerweise fehlende Bilder kennzeichnet.
    Shape imageShape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
    Assert.AreEqual(924, imageShape.ImageData.ImageBytes.Length);

    // Wir können auch einen benutzerdefinierten Rückruf konfigurieren, um alle Warnungen aufgrund von abgelaufenen Webanforderungen abzufangen.
    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[0].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[0].WarningType);
    Assert.AreEqual($"Couldn't load a resource from \'{ImageUrl}\'.", warningCallback.Warnings()[0].Description);

    Assert.AreEqual(WarningSource.Html, warningCallback.Warnings()[1].Source);
    Assert.AreEqual(WarningType.DataLoss, warningCallback.Warnings()[1].WarningType);
    Assert.AreEqual("Image has been replaced with a placeholder.", warningCallback.Warnings()[1].Description);

    doc.Save(ArtifactsDir + "HtmlLoadOptions.WebRequestTimeout.docx");
}

/// <summary>
/// Speichert alle Warnungen, die während eines Dokumentladevorgangs auftreten, in einer Liste.
/// </summary>
private class ListDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        mWarnings.Add(info);
    }

    public List<WarningInfo> Warnings() { 
        return mWarnings;
    }

    private readonly List<WarningInfo> mWarnings = new List<WarningInfo>();
}
```

### Siehe auch

* class [HtmlLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
