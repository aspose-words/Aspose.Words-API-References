---
title: PageLayoutEvent Enum
linktitle: PageLayoutEvent
articleTitle: PageLayoutEvent
second_title: Aspose.Words für .NET
description: Aspose.Words.Layout.PageLayoutEvent opsomming. Ein Ereigniscode der während der Erstellung und Darstellung des Seitenlayoutmodells ausgelöst wird in C#.
type: docs
weight: 3370
url: /de/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

Ein Ereigniscode, der während der Erstellung und Darstellung des Seitenlayoutmodells ausgelöst wird.

Das Seitenlayoutmodell wird in zwei Schritten erstellt. Erstens, „Konvertierungsschritt“, dabei ruft das Seitenlayout Dokumentinhalte ab und erstellt ein Objektdiagramm. Zweitens, „Reflow-Schritt“, dabei werden Strukturen geteilt, zusammengeführt und angeordnet in Seiten.

Abhängig von der Operation, die den Build ausgelöst hat, kann das Seitenlayoutmodell möglicherweise weiter in ein festes Seitenformat gerendert werden. Beispielsweise erfordert die Berechnung der Anzahl der Seiten im Dokument oder das Aktualisieren von Feldern kein Rendern, während dies beim Export in PDF der Fall ist.

```csharp
public enum PageLayoutEvent
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Standardwert |
| WatchDog | `1` | Entspricht einem Prüfpunkt im Code, der häufig besucht wird und zum Abbrechen des Prozesses geeignet ist. |
| BuildStarted | `2` | Der Aufbau des Seitenlayouts hat begonnen. Einmal ausgelöst. Dies ist das erste Ereignis, das auftritt, wenn[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) heißt. |
| BuildFinished | `3` | Die Erstellung des Seitenlayouts ist abgeschlossen. Einmal ausgelöst. Dies ist das letzte Ereignis, das auftritt, wenn[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) heißt. |
| ConversionStarted | `4` | Die Konvertierung des Dokumentmodells in das Seitenlayout hat begonnen. Wird einmal ausgelöst. Dies tritt auf, wenn das Layoutmodell mit dem Abrufen von Dokumentinhalten beginnt. |
| ConversionFinished | `5` | Die Konvertierung des Dokumentmodells in das Seitenlayout ist abgeschlossen. Wird einmal ausgelöst. Dies tritt auf, wenn das Layoutmodell aufhört, Dokumentinhalte abzurufen. |
| ReflowStarted | `6` | Der Reflow des Seitenlayouts hat begonnen. Wird einmal ausgelöst. Dies tritt auf, wenn das Layoutmodell mit dem Umfließen von Dokumentinhalten beginnt. |
| ReflowFinished | `7` | Der Reflow des Seitenlayouts ist abgeschlossen. Wird einmal ausgelöst. Dies tritt auf, wenn das Layoutmodell den Dokumentinhalt nicht mehr umfließt. |
| PartReflowStarted | `8` | Der Neufluss der Seite hat begonnen. Beachten Sie, dass die Seite möglicherweise mehrmals umgebrochen wird und dass der Neufluss möglicherweise erneut beginnt, bevor sie abgeschlossen ist. |
| PartReflowFinished | `9` | Der Seitenumbruch ist abgeschlossen. Beachten Sie, dass die Seite möglicherweise mehrere Male umgebrochen wird und dass der Seitenumbruch erneut erfolgen kann, bevor er abgeschlossen ist. |
| PartRenderingStarted | `10` | Das Rendern der Seite wurde gestartet. Dies wird einmal pro Seite ausgelöst. |
| PartRenderingFinished | `11` | Das Rendern der Seite ist abgeschlossen. Dies wird einmal pro Seite ausgelöst. |

## Beispiele

Zeigt, wie Layoutänderungen mit einem Layout-Callback verfolgt werden.

```csharp
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
/// und rendert eine Seite, auf der wir einen Seiten-Reflow durchführen, in ein Bild im lokalen Dateisystem.
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
