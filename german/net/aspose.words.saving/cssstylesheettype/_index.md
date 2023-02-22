---
title: Enum CssStyleSheetType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.CssStyleSheetType opsomming. Gibt an wie CSSStile Cascading Style Sheet nach HTML exportiert werden.
type: docs
weight: 4630
url: /de/net/aspose.words.saving/cssstylesheettype/
---
## CssStyleSheetType enumeration

Gibt an, wie CSS-Stile (Cascading Style Sheet) nach HTML exportiert werden.

```csharp
public enum CssStyleSheetType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Inline | `0` | CSS-Stile werden inline geschrieben (als Wert der **Stil** Attribut auf jedem Element). |
| Embedded | `1` | CSS-Stile werden getrennt vom Inhalt in ein Stylesheet geschrieben, das in die HTML-Datei eingebettet ist. |
| External | `2` | CSS-Stile werden getrennt vom Inhalt eines Stylesheets in eine externe Datei geschrieben. Die HTML-Datei verlinkt das Stylesheet. |

### Beispiele

Zeigt, wie Sie mit CSS-Stylesheets arbeiten, die eine HTML-Konvertierung erstellt.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Erstellen Sie ein "HtmlFixedSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
    // um zu ändern, wie wir das Dokument in HTML konvertieren.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Legen Sie die Eigenschaft "CssStylesheetType" auf "CssStyleSheetType.External" fest
    // ein gespeichertes HTML-Dokument mit einer externen CSS-Stylesheet-Datei begleiten.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // Im Folgenden finden Sie zwei Möglichkeiten, Verzeichnisse und Dateinamen für Ausgabe-CSS-Stylesheets anzugeben.
    // 1 - Verwenden Sie die Eigenschaft "CssStyleSheetFileName", um unserem Stylesheet einen Dateinamen zuzuweisen:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 - Verwenden Sie einen benutzerdefinierten Callback, um unser Stylesheet zu benennen:
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
        // Über die Eigenschaft "Document" können wir auf das gesamte Quelldokument zugreifen.
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


