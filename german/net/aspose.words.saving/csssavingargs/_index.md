---
title: Class CssSavingArgs
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.CssSavingArgs klas. Stellt Daten für die bereitCssSaving event.
type: docs
weight: 4880
url: /de/net/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class

Stellt Daten für die bereit[`CssSaving`](../icsssavingcallback/csssaving/) event.

Um mehr zu erfahren, besuchen Sie die[Speichern Sie ein Dokument](https://docs.aspose.com/words/net/save-a-document/) Dokumentationsartikel.

```csharp
public class CssSavingArgs
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CssStream](../../aspose.words.saving/csssavingargs/cssstream/) { get; set; } | Ermöglicht die Angabe des Streams, in dem die CSS-Informationen gespeichert werden. |
| [Document](../../aspose.words.saving/csssavingargs/document/) { get; } | Ruft das Dokumentobjekt ab, das gerade gespeichert wird. |
| [IsExportNeeded](../../aspose.words.saving/csssavingargs/isexportneeded/) { get; set; } | Ermöglicht die Angabe, ob das CSS in eine Datei exportiert und in ein HTML-Dokument eingebettet wird. Standard ist`WAHR` . Wenn diese Eigenschaft ist`FALSCH` , die CSS-Informationen werden nicht in einer CSS-Datei gespeichert und nicht in ein HTML-Dokument eingebettet. |
| [KeepCssStreamOpen](../../aspose.words.saving/csssavingargs/keepcssstreamopen/) { get; set; } | Gibt an, ob Aspose.Words den Stream offen halten oder schließen soll, nachdem eine CSS-Information gespeichert wurde. |

### Bemerkungen

Wenn Aspose.Words ein Dokument im HTML-Format speichert, speichert es standardmäßig CSS-Informationen inline (als Wert von **Stil** Attribut für jedes Element).

`CssSavingArgs`Ermöglicht das Speichern von CSS-Informationen in einer Datei, indem Sie Ihr eigenes Stream-Objekt bereitstellen.

Um CSS im Stream zu speichern, verwenden Sie die[`CssStream`](./cssstream/) Eigentum.

Um das Speichern von CSS in einer Datei und das Einbetten in ein HTML-Dokument zu unterdrücken, verwenden Sie die[`IsExportNeeded`](./isexportneeded/) Eigentum.

### Beispiele

Zeigt, wie mit CSS-Stylesheets gearbeitet wird, die bei einer HTML-Konvertierung erstellt werden.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Erstellen Sie ein „HtmlFixedSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
    // um zu ändern, wie wir das Dokument in HTML konvertieren.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Setzen Sie die Eigenschaft „CssStylesheetType“ auf „CssStyleSheetType.External“.
    // ein gespeichertes HTML-Dokument mit einer externen CSS-Stylesheet-Datei ergänzen.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // Nachfolgend finden Sie zwei Möglichkeiten, Verzeichnisse und Dateinamen für Ausgabe-CSS-Stylesheets anzugeben.
    // 1 – Verwenden Sie die Eigenschaft „CssStyleSheetFileName“, um unserem Stylesheet einen Dateinamen zuzuweisen:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 – Verwenden Sie einen benutzerdefinierten Rückruf, um unser Stylesheet zu benennen:
    options.CssSavingCallback =
        new CustomCssSavingCallback(ArtifactsDir + "SavingCallback.ExternalCssFilenames.css", true, false);

    doc.Save(ArtifactsDir + "SavingCallback.ExternalCssFilenames.html", options);
}

/// <summary>
/// Legt einen benutzerdefinierten Dateinamen zusammen mit anderen Parametern für ein externes CSS-Stylesheet fest.
/// </summary>
private class CustomCssSavingCallback : ICssSavingCallback
{
    public CustomCssSavingCallback(string cssDocFilename, bool isExportNeeded, bool keepCssStreamOpen)
    {
        mCssTextFileName = cssDocFilename;
        mIsExportNeeded = isExportNeeded;
        mKeepCssStreamOpen = keepCssStreamOpen;
    }

    public void CssSaving(CssSavingArgs args)
    {
        // Über die Eigenschaft „Document“ können wir auf das gesamte Quelldokument zugreifen.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        args.CssStream = new FileStream(mCssTextFileName, FileMode.Create);
        args.IsExportNeeded = mIsExportNeeded;
        args.KeepCssStreamOpen = mKeepCssStreamOpen;

        Assert.True(args.CssStream.CanWrite);
    }

    private readonly string mCssTextFileName;
    private readonly bool mIsExportNeeded;
    private readonly bool mKeepCssStreamOpen;
}
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


