---
title: FontSettings.DefaultInstance
linktitle: DefaultInstance
articleTitle: DefaultInstance
second_title: Aspose.Words für .NET
description: Entdecken Sie die FontSettings DefaultInstance-Eigenschaft für eine optimierte Verwaltung statischer Schriftarten. Optimieren Sie Ihr Design mit anpassbaren Standardeinstellungen!
type: docs
weight: 20
url: /de/net/aspose.words.fonts/fontsettings/defaultinstance/
---
## FontSettings.DefaultInstance property

Statische Standardschrifteinstellungen.

```csharp
public static FontSettings DefaultInstance { get; }
```

## Bemerkungen

Diese Instanz wird standardmäßig in einem Dokument verwendet, es sei denn[`FontSettings`](../../../aspose.words/document/fontsettings/) ist angegeben.

## Beispiele

Zeigt, wie die Instanz mit den Standardschriftarteinstellungen konfiguriert wird.

```csharp
// Konfigurieren Sie die Standardinstanz für die Schriftarteinstellungen so, dass die Schriftart „Courier New“ verwendet wird
// als Backup-Ersatz, wenn wir versuchen, eine unbekannte Schriftart zu verwenden.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.Enabled);

Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

// Dieses Dokument verfügt nicht über eine FontSettings-Konfiguration. Wenn wir das Dokument rendern,
// Die Standardinstanz von FontSettings behebt die fehlende Schriftart.
// Aspose.Words verwendet „Courier New“, um Text zu rendern, der die unbekannte Schriftart verwendet.
Assert.Null(doc.FontSettings);

doc.Save(ArtifactsDir + "FontSettings.DefaultFontInstance.pdf");
```

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

### Siehe auch

* class [FontSettings](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
