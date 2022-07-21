---
title: WarningCallback
second_title: Aspose.Words für .NET-API-Referenz
description: Wird während verschiedener Dokumentverarbeitungsvorgänge aufgerufen wenn ein Problem erkannt wird das zu einem Verlust der Daten oder der Formatierung führen kann.
type: docs
weight: 90
url: /de/net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

Wird während verschiedener Dokumentverarbeitungsvorgänge aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten oder der Formatierung führen kann.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### Bemerkungen

Das Dokument kann in jeder Phase seines Bestehens Warnungen generieren, daher ist es wichtig, den Warnungsrückruf so so früh wie möglich einzurichten, um den Verlust von Warnungen zu vermeiden. ZB solche Eigenschaften wie[`PageCount`](../../document/pagecount) erstellt tatsächlich das Dokumentlayout, das später zum Rendern verwendet wird, und die Layout-Warnungen können verloren gehen, wenn der Warnrückruf nur für die späteren Rendering-Aufrufe angegeben wird.

### Beispiele

Zeigt, wie die IWarningCallback-Schnittstelle zum Überwachen von Schriftartersetzungswarnungen verwendet wird.

```csharp
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

    // Zu Testzwecken werden wir Aspose.Words so einstellen, dass es nur in einem Ordner nach Schriftarten sucht, der nicht existiert.
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // Beim Rendern des Dokuments gibt es keinen Platz, um die Schriftart "Times New Roman" zu finden.
    // Dies führt zu einer Schriftartersetzungswarnung, die unser Callback erkennt.
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// Wird jedes Mal aufgerufen, wenn während des Ladens/Speicherns eine Warnung auftritt.
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
[Test]
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

    // Wir erhalten eine Schriftersetzungswarnung, wenn wir ein Dokument mit einer fehlenden Schrift speichern.
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
    /// Wird jedes Mal aufgerufen, wenn während des Ladens/Speicherns eine Warnung auftritt.
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

* interface [IWarningCallback](../../iwarningcallback)
* class [DocumentBase](../../documentbase)
* namensraum [Aspose.Words](../../documentbase)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
