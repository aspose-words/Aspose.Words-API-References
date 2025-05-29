---
title: PageSavingArgs Class
linktitle: PageSavingArgs
articleTitle: PageSavingArgs
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Saving.PageSavingArgs, die für die Optimierung der Dokumentverarbeitung mit detaillierten PageSaving-Ereignisdaten unerlässlich ist. Verbessern Sie Ihren Workflow!
type: docs
weight: 6160
url: /de/net/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class

Liefert Daten für die[`PageSaving`](../ipagesavingcallback/pagesaving/) Ereignis.

Um mehr zu erfahren, besuchen Sie die[Programmieren mit Dokumenten](https://docs.aspose.com/words/net/programming-with-documents/) Dokumentationsartikel.

```csharp
public class PageSavingArgs
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [PageSavingArgs](pagesavingargs/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [KeepPageStreamOpen](../../aspose.words.saving/pagesavingargs/keeppagestreamopen/) { get; set; } | Gibt an, ob Aspose.Words den Stream nach dem Speichern einer Dokumentseite geöffnet lassen oder schließen soll. |
| [PageFileName](../../aspose.words.saving/pagesavingargs/pagefilename/) { get; set; } | Ruft den Dateinamen ab, unter dem die Dokumentseite gespeichert wird, oder legt diesen fest. |
| [PageIndex](../../aspose.words.saving/pagesavingargs/pageindex/) { get; } | Aktueller Seitenindex. |
| [PageStream](../../aspose.words.saving/pagesavingargs/pagestream/) { get; set; } | Ermöglicht die Angabe des Streams, in dem die Dokumentseite gespeichert wird. |

## Beispiele

Zeigt, wie Sie mithilfe eines Rückrufs ein Dokument seitenweise im HTML-Format speichern.

```csharp
public void PageFileNames()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Page 1.");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 2.");
    builder.InsertImage(ImageDir + "Logo.jpg");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 3.");

    // Erstellen Sie ein "HtmlFixedSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
    // um zu ändern, wie wir das Dokument in HTML konvertieren.
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // Wir speichern jede Seite dieses Dokuments in einer separaten HTML-Datei im lokalen Dateisystem.
    // Legen Sie einen Rückruf fest, der es uns ermöglicht, jedes ausgegebene HTML-Dokument zu benennen.
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// Speichert alle Seiten in einer darin angegebenen Datei und einem angegebenen Verzeichnis.
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // Unten finden Sie zwei Möglichkeiten, anzugeben, wo Aspose.Words jede Seite des Dokuments speichert.
        // 1 – Legen Sie einen Dateinamen für die Ausgabeseitendatei fest:
        args.PageFileName = outFileName;

        // 2 – Erstellen Sie einen benutzerdefinierten Stream für die Ausgabeseitendatei:
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
