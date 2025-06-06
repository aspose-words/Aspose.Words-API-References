---
title: HtmlSaveOptions.CssStyleSheetFileName
linktitle: CssStyleSheetFileName
articleTitle: CssStyleSheetFileName
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „HtmlSaveOptions CssStyleSheetFileName“ Ihre HTML-Exporte mit einem angegebenen CSS-Dateipfad anpasst und so den Stil Ihres Dokuments verbessert.
type: docs
weight: 50
url: /de/net/aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/
---
## HtmlSaveOptions.CssStyleSheetFileName property

Gibt den Pfad und den Namen der Cascading Style Sheet (CSS)-Datei an, die geschrieben wird, wenn ein Dokument nach HTML exportiert wird. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string CssStyleSheetFileName { get; set; }
```

## Bemerkungen

Diese Eigenschaft hat nur dann eine Auswirkung, wenn ein Dokument im HTML-Format gespeichert wird und ein externes CSS-Stylesheet mit[`CssStyleSheetType`](../cssstylesheettype/).

Wenn diese Eigenschaft leer ist, wird die CSS-Datei im selben Ordner und unter demselben Namen wie das HTML -Dokument gespeichert, jedoch mit der Erweiterung „.css“.

Wenn in dieser Eigenschaft nur der Pfad, aber kein Dateiname angegeben ist, wird die CSS-Datei im angegebenen Ordner gespeichert und hat denselben Namen wie das HTML-Dokument, jedoch mit der Erweiterung „.css“.

Wenn der durch diese Eigenschaft angegebene Ordner nicht existiert, wird er automatisch erstellt, bevor die CSS-Datei gespeichert wird.

Eine weitere Möglichkeit, einen Ordner anzugeben, in dem externe CSS-Dateien gespeichert werden, ist die Verwendung von[`ResourceFolder`](../resourcefolder/) .

## Beispiele

Zeigt, wie mit CSS-Stylesheets gearbeitet wird, die bei einer HTML-Konvertierung erstellt werden.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Erstellen Sie ein "HtmlFixedSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
    // um zu ändern, wie wir das Dokument in HTML konvertieren.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Setzen Sie die Eigenschaft "CssStylesheetType" auf "CssStyleSheetType.External", um
    // Begleiten Sie ein gespeichertes HTML-Dokument mit einer externen CSS-Stylesheet-Datei.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // Unten finden Sie zwei Möglichkeiten zum Angeben von Verzeichnissen und Dateinamen für die Ausgabe von CSS-Stylesheets.
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
        // Über die Eigenschaft „Dokument“ können wir auf das gesamte Quelldokument zugreifen.
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

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
