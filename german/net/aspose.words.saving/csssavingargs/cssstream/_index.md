---
title: CssSavingArgs.CssStream
linktitle: CssStream
articleTitle: CssStream
second_title: Aspose.Words für .NET
description: CssSavingArgs CssStream eigendom. Ermöglicht die Angabe des Streams in dem die CSSInformationen gespeichert werden in C#.
type: docs
weight: 10
url: /de/net/aspose.words.saving/csssavingargs/cssstream/
---
## CssSavingArgs.CssStream property

Ermöglicht die Angabe des Streams, in dem die CSS-Informationen gespeichert werden.

```csharp
public Stream CssStream { get; set; }
```

## Bemerkungen

Mit dieser Eigenschaft können Sie CSS-Informationen in einem Stream speichern.

Der Standardwert ist`Null` . Diese Eigenschaft unterdrückt nicht das Speichern von CSS-Informationen in einer Datei oder das Einbetten in ein HTML-Dokument. Um den Export von CSS zu unterdrücken, verwenden Sie die[`IsExportNeeded`](../isexportneeded/) Eigentum.

Benutzen[`ICssSavingCallback`](../../icsssavingcallback/) Sie können CSS nicht durch ein anderes ersetzen. Es ist nur zum Speichern von CSS in einem Stream gedacht.

## Beispiele

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

* class [CssSavingArgs](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
