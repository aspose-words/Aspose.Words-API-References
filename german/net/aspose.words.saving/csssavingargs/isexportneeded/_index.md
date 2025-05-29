---
title: CssSavingArgs.IsExportNeeded
linktitle: IsExportNeeded
articleTitle: IsExportNeeded
second_title: Aspose.Words für .NET
description: Steuern Sie den CSS-Export mit der IsExportNeeded-Eigenschaft von CssSavingArgs. Wählen Sie, ob CSS eingebettet oder in einer Datei gespeichert werden soll, um HTML-Dokumente zu optimieren. Standardmäßig „true“.
type: docs
weight: 30
url: /de/net/aspose.words.saving/csssavingargs/isexportneeded/
---
## CssSavingArgs.IsExportNeeded property

Hier können Sie festlegen, ob das CSS in eine Datei exportiert und in ein HTML-Dokument eingebettet wird. Standardmäßig ist`WAHR` . Wenn diese Eigenschaft`FALSCH` , die CSS-Informationen werden nicht in einer CSS-Datei gespeichert und nicht in ein HTML-Dokument eingebettet.

```csharp
public bool IsExportNeeded { get; set; }
```

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

* class [CssSavingArgs](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
