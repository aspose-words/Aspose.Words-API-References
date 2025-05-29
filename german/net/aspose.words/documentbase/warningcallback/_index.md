---
title: DocumentBase.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words für .NET
description: Entdecken Sie die DocumentBase WarningCallback-Eigenschaft, die für die Gewährleistung der Datenintegrität während der Dokumentverarbeitung durch Erkennung potenzieller Formatierungsprobleme von entscheidender Bedeutung ist.
type: docs
weight: 100
url: /de/net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

Wird während verschiedener Dokumentverarbeitungsverfahren aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten- oder Formatierungsgenauigkeit führen kann.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Bemerkungen

Dokumente können in jeder Phase ihrer Existenz Warnungen generieren. Daher ist es wichtig, den Warn-Callback so früh wie möglich einzurichten, um den Verlust von Warnungen zu vermeiden. Beispielsweise können Eigenschaften wie[`PageCount`](../../document/pagecount/) tatsächlich das Dokumentlayout erstellen, das später zum Rendern verwendet wird, und die Layoutwarnungen können verloren gehen, wenn der Warnungsrückruf nur für die späteren Renderaufrufe angegeben wird.

## Beispiele

Zeigt, wie die IWarningCallback-Schnittstelle zum Überwachen von Schriftartersetzungswarnungen verwendet wird.

```csharp
public void SubstitutionWarning()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // Speichert die aktuelle Sammlung von Schriftartquellen, die als Standardschriftartquelle für jedes Dokument dienen.
    // für die wir keine andere Schriftartquelle angeben.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // Zu Testzwecken stellen wir Aspose.Words so ein, dass nur in einem Ordner nach Schriftarten gesucht wird, der nicht existiert.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // Beim Rendern des Dokuments ist die Schriftart „Times New Roman“ nirgends zu finden.
    // Dies führt zu einer Warnung bezüglich der Schriftartersetzung, die von unserem Rückruf erkannt wird.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].WarningType == WarningType.FontSubstitution);
    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// Wird jedes Mal aufgerufen, wenn beim Laden/Speichern eine Warnung auftritt.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

Zeigt, wie die Eigenschaft zum Suchen der besten Entsprechung für eine fehlende Schriftart aus den verfügbaren Schriftartquellen festgelegt wird.

```csharp
public void EnableFontSubstitution()
{
    // Öffnen Sie ein Dokument, das Text enthält, der mit einer Schriftart formatiert ist, die in keiner unserer Schriftartquellen vorhanden ist.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Weisen Sie einen Rückruf für die Behandlung von Warnungen zur Schriftartersetzung zu.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Legen Sie einen Standardschriftnamen fest und aktivieren Sie die Schriftartersetzung.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Nach der Schriftartersetzung sollten die ursprünglichen Schriftmaße verwendet werden.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // Wir erhalten eine Warnung zur Schriftartersetzung, wenn wir ein Dokument mit einer fehlenden Schriftart speichern.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // Wir können auch Warnungen in der Sammlung überprüfen und löschen.
    Assert.AreEqual(WarningSource.Layout, substitutionWarningHandler.FontWarnings[0].Source);
    Assert.AreEqual(
        "Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
        substitutionWarningHandler.FontWarnings[0].Description);

    substitutionWarningHandler.FontWarnings.Clear();

    Assert.AreEqual(0, substitutionWarningHandler.FontWarnings.Count);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Wird jedes Mal aufgerufen, wenn beim Laden/Speichern eine Warnung auftritt.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontWarnings.Warning(info);
    }

    public WarningInfoCollection FontWarnings = new WarningInfoCollection();
}
```

### Siehe auch

* interface [IWarningCallback](../../iwarningcallback/)
* class [DocumentBase](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
