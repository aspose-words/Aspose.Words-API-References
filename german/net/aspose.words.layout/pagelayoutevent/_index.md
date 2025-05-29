---
title: PageLayoutEvent Enum
linktitle: PageLayoutEvent
articleTitle: PageLayoutEvent
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Layout.PageLayoutEvent – unerlässlich für die Optimierung von Seitenlayout-Ereignissen beim Rendern und Erstellen von Dokumenten. Verbessern Sie Ihren Workflow noch heute!
type: docs
weight: 3820
url: /de/net/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enumeration

Ein Ereigniscode, der während der Erstellung und Darstellung des Seitenlayoutmodells ausgelöst wird.

Das Seitenlayoutmodell wird in zwei Schritten erstellt. Erstens: „Konvertierungsschritt“. Dabei zieht das Seitenlayout Dokumentinhalte und erstellt ein Objektdiagramm. Zweitens: „Reflow-Schritt“. Dabei werden Strukturen aufgeteilt, zusammengeführt und in Seiten angeordnet.

Abhängig von der Operation, die den Build ausgelöst hat, kann das Seitenlayoutmodell weiter in ein festes Seitenformat gerendert werden oder nicht. Beispielsweise erfordert das Berechnen der Seitenanzahl im Dokument oder das Aktualisieren von Feldern kein Rendering, wohingegen dies beim Export ins PDF-Format erforderlich ist.

```csharp
public enum PageLayoutEvent
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Standardwert |
| WatchDog | `1` | Entspricht einem Prüfpunkt im Code, der häufig besucht wird und zum Abbruch des Prozesses geeignet ist. |
| BuildStarted | `2` | Der Aufbau des Seitenlayouts wurde gestartet. Einmal ausgelöst. Dies ist das erste Ereignis, das auftritt, wenn[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) heißt. |
| BuildFinished | `3` | Der Aufbau des Seitenlayouts ist abgeschlossen. Einmal ausgelöst. Dies ist das letzte Ereignis, das auftritt, wenn[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/) heißt. |
| ConversionStarted | `4` | Die Konvertierung des Dokumentmodells in das Seitenlayout wurde gestartet. Einmal ausgelöst. Dies geschieht, wenn das Layoutmodell beginnt, Dokumentinhalte abzurufen. |
| ConversionFinished | `5` | Die Konvertierung des Dokumentmodells in das Seitenlayout ist abgeschlossen. Einmal ausgelöst. Dies geschieht, wenn das Layoutmodell aufhört, Dokumentinhalte abzurufen. |
| ReflowStarted | `6` | Das Umfließen des Seitenlayouts wurde gestartet. Einmal ausgelöst. Dies geschieht, wenn das Layoutmodell mit dem Umfließen des Dokumentinhalts beginnt. |
| ReflowFinished | `7` | Das Umfließen des Seitenlayouts ist abgeschlossen. Wird einmal ausgelöst. Dies geschieht, wenn das Layoutmodell das Umfließen des Dokumentinhalts beendet. |
| PartReflowStarted | `8` | Der Seitenumbruch wurde gestartet. Beachten Sie, dass der Seitenumbruch möglicherweise mehrmals erfolgt und dass der Umbruch möglicherweise neu gestartet wird, bevor er abgeschlossen ist. |
| PartReflowFinished | `9` | Der Seitenumbruch ist abgeschlossen. Beachten Sie, dass der Seitenumbruch möglicherweise mehrmals erfolgt und dass der Umbruch möglicherweise neu gestartet wird, bevor er abgeschlossen ist. |
| PartRenderingStarted | `10` | Das Rendern der Seite wurde gestartet. Dies wird einmal pro Seite ausgelöst. |
| PartRenderingFinished | `11` | Das Rendern der Seite ist abgeschlossen. Dies wird einmal pro Seite ausgelöst. |

## Beispiele

Zeigt, wie Layoutänderungen mit einem Layout-Rückruf verfolgt werden.

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
/// und rendert eine Seite, auf der wir einen Seitenumbruch in ein Bild im lokalen Dateisystem durchführen.
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
