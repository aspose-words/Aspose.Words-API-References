---
title: DocumentBase.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words für .NET
description: DocumentBase WarningCallback eigendom. Wird während verschiedener Dokumentverarbeitungsvorgänge aufgerufen wenn ein Problem erkannt wird das zu einem Verlust der Daten oder Formatierungstreue führen könnte in C#.
type: docs
weight: 90
url: /de/net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

Wird während verschiedener Dokumentverarbeitungsvorgänge aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten- oder Formatierungstreue führen könnte.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Bemerkungen

Das Dokument kann in jedem Stadium seiner Existenz Warnungen generieren. Daher ist es wichtig, den Warnungsrückruf so früh wie möglich einzurichten, um den Verlust der Warnungen zu vermeiden. ZB solche Eigenschaften wie[`PageCount`](../../document/pagecount/) erstellt tatsächlich das Dokumentlayout, das später zum Rendern verwendet wird, und die Layoutwarnungen gehen möglicherweise verloren, wenn der Warnungsrückruf nur für die späteren Rendering-Aufrufe angegeben wird.

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

    // Speichern Sie die aktuelle Sammlung von Schriftartquellen, die die Standardschriftquelle für jedes Dokument sein wird
    // für die wir keine andere Schriftartquelle angeben.
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // Zu Testzwecken stellen wir Aspose.Words so ein, dass es nur in einem Ordner nach Schriftarten sucht, der nicht existiert.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // Beim Rendern des Dokuments ist die Schriftart „Times New Roman“ nicht zu finden.
    // Dies führt zu einer Schriftartersetzungswarnung, die unser Rückruf erkennt.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].WarningType == WarningType.FontSubstitution);
    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font.", StringComparison.Ordinal));
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

Zeigt, wie die Eigenschaft festgelegt wird, um die beste Übereinstimmung für eine fehlende Schriftart aus den verfügbaren Schriftartquellen zu finden.

```csharp
public void EnableFontSubstitution()
{
    // Öffnen Sie ein Dokument, das Text enthält, der mit einer Schriftart formatiert ist, die in keiner unserer Schriftartquellen vorhanden ist.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Weisen Sie einen Rückruf für die Behandlung von Schriftartersetzungswarnungen zu.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Legen Sie einen Standardschriftnamen fest und aktivieren Sie die Schriftartersetzung.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Nach der Schriftartersetzung sollten die ursprünglichen Schriftartmetriken verwendet werden.
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

    Assert.That(substitutionWarningHandler.FontWarnings, Is.Empty);
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
