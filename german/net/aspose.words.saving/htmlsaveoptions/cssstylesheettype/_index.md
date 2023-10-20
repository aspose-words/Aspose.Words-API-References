---
title: HtmlSaveOptions.CssStyleSheetType
linktitle: CssStyleSheetType
articleTitle: CssStyleSheetType
second_title: Aspose.Words für .NET
description: HtmlSaveOptions CssStyleSheetType eigendom. Gibt an wie CSSStile Cascading Style Sheet nach HTML MHTML oder EPUB exportiert werden. Der Standardwert istInline für HTML/MHTML und External für EPUB in C#.
type: docs
weight: 60
url: /de/net/aspose.words.saving/htmlsaveoptions/cssstylesheettype/
---
## HtmlSaveOptions.CssStyleSheetType property

Gibt an, wie CSS-Stile (Cascading Style Sheet) nach HTML, MHTML oder EPUB exportiert werden. Der Standardwert istInline für HTML/MHTML und External für EPUB.

```csharp
public CssStyleSheetType CssStyleSheetType { get; set; }
```

## Bemerkungen

Das Speichern von CSS-Stylesheets in einer externen Datei wird nur beim Speichern in HTML unterstützt. Wenn Sie in eines der Containerformate (EPUB oder MHTML) exportieren und angebenExternal, wird die CSS-Datei in das Ausgabepaket gekapselt.

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

* property [CssStyleSheetFileName](../cssstylesheetfilename/)
* enum [CssStyleSheetType](../../cssstylesheettype/)
* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
