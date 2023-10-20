---
title: FontSettings.DefaultInstance
linktitle: DefaultInstance
articleTitle: DefaultInstance
second_title: Aspose.Words für .NET
description: FontSettings DefaultInstance eigendom. Statische StandardSchriftarteinstellungen in C#.
type: docs
weight: 20
url: /de/net/aspose.words.fonts/fontsettings/defaultinstance/
---
## FontSettings.DefaultInstance property

Statische Standard-Schriftarteinstellungen.

```csharp
public static FontSettings DefaultInstance { get; }
```

## Bemerkungen

Diese Instanz wird standardmäßig in einem Dokument verwendet, sofern nicht[`FontSettings`](../../../aspose.words/document/fontsettings/) angegeben ist.

## Beispiele

Zeigt, wie die Instanz der Standardschriftarteinstellungen konfiguriert wird.

```csharp
// Konfigurieren Sie die Standard-Schriftarteinstellungsinstanz für die Verwendung der Schriftart „Courier New“.
// als Backup-Ersatz, wenn wir versuchen, eine unbekannte Schriftart zu verwenden.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.Enabled);

Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

// Dieses Dokument verfügt über keine FontSettings-Konfiguration. Wenn wir das Dokument rendern,
// Die Standardinstanz von FontSettings löst die fehlende Schriftart auf.
// Aspose.Words verwendet „Courier New“, um Text darzustellen, der die unbekannte Schriftart verwendet.
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

### Siehe auch

* class [FontSettings](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
