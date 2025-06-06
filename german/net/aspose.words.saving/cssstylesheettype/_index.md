---
title: CssStyleSheetType Enum
linktitle: CssStyleSheetType
articleTitle: CssStyleSheetType
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Aspose.Words.CssStyleSheetType den HTML-Export verbessert, indem es CSS-Stile für eine bessere Webpräsentation und Leistung optimiert.
type: docs
weight: 5630
url: /de/net/aspose.words.saving/cssstylesheettype/
---
## CssStyleSheetType enumeration

Gibt an, wie CSS-Stile (Cascading Style Sheet) in HTML exportiert werden.

```csharp
public enum CssStyleSheetType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Inline | `0` | CSS-Stile werden inline geschrieben (als Wert des**Stil** Attribut für jedes Element). |
| Embedded | `1` | CSS-Stile werden getrennt vom Inhalt in einem in die HTML-Datei eingebetteten Stylesheet geschrieben. |
| External | `2` | CSS-Stile werden getrennt vom Inhalt in einem Stylesheet in einer externen Datei geschrieben. Die HTML-Datei verknüpft das Stylesheet. |

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

* property [CssStyleSheetType](../htmlsaveoptions/cssstylesheettype/)
* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
