---
title: FontSubstitutionSettings.FontInfoSubstitution
linktitle: FontInfoSubstitution
articleTitle: FontInfoSubstitution
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie FontSubstitutionSettings Ihre Typografie mit anpassbaren Schriftinformationsregeln für verbessertes Design und Lesbarkeit verbessert.
type: docs
weight: 30
url: /de/net/aspose.words.fonts/fontsubstitutionsettings/fontinfosubstitution/
---
## FontSubstitutionSettings.FontInfoSubstitution property

Einstellungen im Zusammenhang mit der Regel zur Ersetzung von Schriftinformationen.

```csharp
public FontInfoSubstitutionRule FontInfoSubstitution { get; }
```

## Beispiele

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

* class [FontInfoSubstitutionRule](../../fontinfosubstitutionrule/)
* class [FontSubstitutionSettings](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
