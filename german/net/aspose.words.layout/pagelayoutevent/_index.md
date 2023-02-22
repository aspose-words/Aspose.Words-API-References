---
title: Enum PageLayoutEvent
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Layout.PageLayoutEvent opsomming. Ein Ereigniscode der während des Erstellens und Renderns des Seitenlayoutmodells ausgelöst wird.
type: docs
weight: 3170
url: /de/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

Ein Ereigniscode, der während des Erstellens und Renderns des Seitenlayoutmodells ausgelöst wird.

Das Seitenlayoutmodell wird in zwei Schritten erstellt. Erstens, "Konvertierungsschritt", in diesem Fall zieht das Seitenlayout Dokumentinhalte und erstellt Objektdiagramme. Zweitens, "Reflow-Schritt", in dem Strukturen geteilt, zusammengeführt und angeordnet werden in Seiten.

Abhängig von der Operation, die das Erstellen ausgelöst hat, kann das Seitenlayoutmodell weiter in ein festes Seitenformat gerendert werden oder nicht. Zum Beispiel erfordert das Berechnen der Seitenzahl im Dokument oder das Aktualisieren von Feldern kein Rendering, während der Export nach PDF dies erfordert.

```csharp
public enum PageLayoutEvent
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Standardwert |
| WatchDog | `1` | Entspricht einem häufig besuchten Checkpoint im Code, der zum Abbruch des Prozesses geeignet ist. |
| BuildStarted | `2` | Der Aufbau des Seitenlayouts hat begonnen. Einmal ausgelöst. Dies ist das erste Ereignis, das auftritt, wenn[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) heißt. |
| BuildFinished | `3` | Der Aufbau des Seitenlayouts ist abgeschlossen. Einmal ausgelöst. Dies ist das letzte Ereignis, das wann auftritt[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) heißt. |
| ConversionStarted | `4` | Die Konvertierung des Dokumentenmodells in das Seitenlayout hat begonnen. Einmal ausgelöst. Dies tritt auf, wenn das Layoutmodell beginnt, Dokumentinhalte abzurufen. |
| ConversionFinished | `5` | Die Konvertierung des Dokumentmodells in das Seitenlayout ist abgeschlossen. Einmal ausgelöst. Dies tritt auf, wenn das Layoutmodell aufhört, Dokumentinhalte abzurufen. |
| ReflowStarted | `6` | Reflow des Seitenlayouts hat begonnen. Einmal ausgelöst. Dies tritt auf, wenn das Layoutmodell beginnt, den Dokumentinhalt umzufließen. |
| ReflowFinished | `7` | Reflow des Seitenlayouts ist abgeschlossen. Einmal ausgelöst. Dies tritt auf, wenn das Layoutmodell das Umfließen des Dokumentinhalts beendet. |
| PartReflowStarted | `8` | Der Neufluss der Seite hat begonnen. Beachten Sie, dass die Seite möglicherweise mehrmals neu umflossen wird und dass der Neufluss möglicherweise neu gestartet wird, bevor er abgeschlossen ist. |
| PartReflowFinished | `9` | Der Seitenumbruch ist abgeschlossen. Beachten Sie, dass die Seite möglicherweise mehrmals umflossen wird und dass der Umbruch möglicherweise neu gestartet wird, bevor sie abgeschlossen ist. |
| PartRenderingStarted | `10` | Das Rendern der Seite hat begonnen. Dies wird einmal pro Seite ausgelöst. |
| PartRenderingFinished | `11` | Das Rendern der Seite ist beendet. Dies wird einmal pro Seite ausgelöst. |

### Beispiele

Zeigt, wie Layoutänderungen mit einem Layout-Callback nachverfolgt werden.

```csharp
[Test]
public void PageLayoutCallback()
{
    Document doc = new Document();
    doc.BuiltInDocumentProperties.Title = "My Document";

    DocumentBuilder builder = new DocumentBuilder(doc);
    builder.Writeln("Hello world!");

    doc.LayoutOptions.Callback = new RenderPageLayoutCallback();
    doc.UpdatePageLayout();

    doc.Save(ArtifactsDir + "Layout.PageLayoutCallback.pdf");
}

/// <summary>
/// Benachrichtigt uns, wenn wir das Dokument in einem festen Seitenformat speichern
/// und rendert eine Seite, auf der wir einen Seitenumbruch zu einem Bild im lokalen Dateisystem durchführen.
/// </summary>
private class RenderPageLayoutCallback : IPageLayoutCallback
{
    public void Notify(PageLayoutCallbackArgs a)
    {
        switch (a.Event)
        {
            case PageLayoutEvent.PartReflowFinished:
                NotifyPartFinished(a);
                break;
            case PageLayoutEvent.ConversionFinished:
                NotifyConversionFinished(a);
                break;
        }
    }

    private void NotifyPartFinished(PageLayoutCallbackArgs a)
    {
        Console.WriteLine($"Part at page {a.PageIndex + 1} reflow.");
        RenderPage(a, a.PageIndex);
    }

    private void NotifyConversionFinished(PageLayoutCallbackArgs a)
    {
        Console.WriteLine($"Document \"{a.Document.BuiltInDocumentProperties.Title}\" converted to page format.");
    }

    private void RenderPage(PageLayoutCallbackArgs a, int pageIndex)
    {
        ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png) { PageSet = new PageSet(pageIndex) };

        using (FileStream stream =
            new FileStream(ArtifactsDir + $@"PageLayoutCallback.page-{pageIndex + 1} {++mNum}.png",
                FileMode.Create))
            a.Document.Save(stream, saveOptions);
    }

    private int mNum;
}
```

### Siehe auch

* namensraum [Aspose.Words.Layout](../../aspose.words.layout/)
* Montage [Aspose.Words](../../)


