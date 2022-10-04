---
title: FontSettings
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt Schriftarteinstellungen für ein Dokument an.
type: docs
weight: 2790
url: /de/net/aspose.words.fonts/fontsettings/
---
## FontSettings class

Gibt Schriftarteinstellungen für ein Dokument an.

```csharp
public class FontSettings
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [FontSettings](fontsettings/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| static [DefaultInstance](../../aspose.words.fonts/fontsettings/defaultinstance/) { get; } | Statische Standardschrifteinstellungen. |
| [FallbackSettings](../../aspose.words.fonts/fontsettings/fallbacksettings/) { get; } | Einstellungen im Zusammenhang mit dem Font-Fallback-Mechanismus. |
| [SubstitutionSettings](../../aspose.words.fonts/fontsettings/substitutionsettings/) { get; } | Einstellungen in Bezug auf den Schriftersetzungsmechanismus. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFontsSources](../../aspose.words.fonts/fontsettings/getfontssources/)() | Ruft eine Kopie des Arrays ab, das die Liste der Quellen enthält, in denen Aspose.Words nach TrueType-Schriftarten sucht. |
| [ResetFontSources](../../aspose.words.fonts/fontsettings/resetfontsources/)() | Setzt die Schriftartquellen auf die Systemvorgabe zurück. |
| [SaveSearchCache](../../aspose.words.fonts/fontsettings/savesearchcache/)(Stream) | Speichert den Schriftsuchcache im Stream. |
| [SetFontsFolder](../../aspose.words.fonts/fontsettings/setfontsfolder/)(string, bool) | Legt den Ordner fest, in dem Aspose.Words beim Rendern von Dokumenten oder beim Einbetten von Schriftarten nach TrueType-Schriftarten sucht. Dies ist eine Verknüpfung zu[`SetFontsFolders`](./setfontsfolders/) zum Setzen nur eines Fontverzeichnisses. |
| [SetFontsFolders](../../aspose.words.fonts/fontsettings/setfontsfolders/)(string[], bool) | Legt die Ordner fest, in denen Aspose.Words beim Rendern von Dokumenten oder beim Einbetten von Schriftarten nach TrueType-Schriftarten sucht. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources)(FontSourceBase[]) | Legt die Quellen fest, in denen Aspose.Words beim Rendern von Dokumenten oder beim Einbetten von Schriftarten nach TrueType-Schriftarten sucht. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources_1)(FontSourceBase[], Stream) | Legt die Quellen fest, in denen Aspose.Words nach TrueType-Schriftarten sucht und lädt zusätzlich zuvor gespeicherte Schriftsuchcache. |

### Bemerkungen

Aspose.Words verwendet Schriftarteinstellungen, um die Schriftarten im Dokument aufzulösen. Schriftarten werden meistens aufgelöst, wenn Dokumentlayout erstellt oder in feste Seitenformate gerendert wird. Aber beim Laden einiger Formate kann Aspose.Words auch verlangen, dass die Schriftarten aufgelöst werden. Wenn beispielsweise beim HTML-Dokumente geladen werden, kann Aspose.Words die Schriftarten auflösen, um eine Fallback-Funktion für Schriftarten auszuführen. Es wird daher empfohlen, die Schriftarteinstellungen in [`LoadOptions`](../../aspose.words.loading/loadoptions/) beim Einlegen des Dokuments. Oder zumindest vor dem Erstellen des Layouts oder dem Rendern des Dokuments in das Festseitenformat.

Standardmäßig verwenden alle Dokumente eine einzige statische Schrifteinstellungsinstanz. Es konnte von darauf zugegriffen werden[`DefaultInstance`](./defaultinstance/) Eigentum.

Das Ändern von Schriftarteinstellungen ist jederzeit sicher von jedem Thread aus möglich. Es wird jedoch empfohlen, die Schriftarteinstellungen nicht zu ändern, während einige Dokumente verarbeitet werden, die diese Einstellungen verwenden. Dies kann dazu führen, dass derselbe Font in verschiedenen Teilen des Dokuments unterschiedlich aufgelöst wird.

### Beispiele

Zeigt, wie eine Schriftartquelle zu unseren vorhandenen Schriftartquellen hinzugefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);

Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Der Standard-Schriftquelle fehlen zwei der Schriftarten, die wir in unserem Dokument verwenden.
// Wenn wir dieses Dokument speichern, wendet Aspose.Words Fallback-Schriftarten auf allen Text an, der mit nicht zugänglichen Schriftarten formatiert ist.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Erstellen Sie eine Schriftartquelle aus einem Ordner, der Schriftarten enthält.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Wenden Sie ein neues Array von Schriftartquellen an, das die ursprünglichen Schriftartquellen sowie unsere benutzerdefinierten Schriftarten enthält.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Stellen Sie sicher, dass Aspose.Words Zugriff auf alle erforderlichen Schriftarten hat, bevor wir das Dokument als PDF rendern.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Stellen Sie die ursprünglichen Schriftartquellen wieder her.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

Zeigt, wie Sie ein Quellenverzeichnis für Schriftarten festlegen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Unsere Schriftartquellen enthalten nicht die Schriftart, die wir für Text in diesem Dokument verwendet haben.
// Wenn wir diese Schriftarteinstellungen beim Rendern dieses Dokuments verwenden,
// Aspose.Words wendet eine Fallback-Schriftart auf Text an, der eine Schriftart hat, die Aspose.Words nicht finden kann.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// In den Standardquellen für Schriftarten fehlen die beiden Schriftarten, die wir in diesem Dokument verwenden.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Verwenden Sie die Methode "SetFontsFolder", um ein Verzeichnis festzulegen, das als neue Schriftartquelle fungiert.
// Übergeben Sie "false" als "rekursives" Argument, um Schriftarten aus allen Schriftartdateien einzubeziehen, die sich im Verzeichnis befinden
// dass wir das erste Argument übergeben, aber keine Schriftarten in einem der Unterordner dieses Verzeichnisses enthalten.
// Übergeben Sie "true" als "rekursives" Argument, um alle Schriftdateien im übergebenen Verzeichnis einzuschließen
// im ersten Argument sowie alle Schriftarten in seinen Unterverzeichnissen.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Die Schriftart "Amethysta" befindet sich in einem Unterordner des Schriftartenverzeichnisses.
if (recursive)
{
    Assert.AreEqual(25, newFontSources[0].GetAvailableFonts().Count);
    Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}
else
{
    Assert.AreEqual(18, newFontSources[0].GetAvailableFonts().Count);
    Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolder.pdf");

// Stellen Sie die ursprünglichen Schriftartquellen wieder her.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

Zeigt, wie Sie mehrere Quellverzeichnisse für Schriftarten festlegen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Unsere Schriftartquellen enthalten nicht die Schriftart, die wir für Text in diesem Dokument verwendet haben.
// Wenn wir diese Schriftarteinstellungen beim Rendern dieses Dokuments verwenden,
// Aspose.Words wendet eine Fallback-Schriftart auf Text an, der eine Schriftart hat, die Aspose.Words nicht finden kann.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// In den Standardquellen für Schriftarten fehlen die beiden Schriftarten, die wir in diesem Dokument verwenden.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Verwenden Sie die Methode "SetFontsFolders", um eine Schriftartquelle aus jedem Schriftartverzeichnis zu erstellen, das wir als erstes Argument übergeben.
// Übergeben Sie "false" als "rekursives" Argument, um Schriftarten aus allen Schriftartdateien einzuschließen, die sich in den Verzeichnissen befinden
// dass wir das erste Argument übergeben, aber keine Schriftarten aus den Unterordnern der Verzeichnisse enthalten.
// Übergeben Sie "true" als "rekursives" Argument, um alle Schriftdateien in den übergebenen Verzeichnissen einzuschließen
// im ersten Argument sowie alle Schriftarten in ihren Unterverzeichnissen.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Der "Junction"-Ordner selbst enthält keine Schriftdateien, hat aber Unterordner, die dies tun.
if (recursive)
{
    Assert.AreEqual(6, newFontSources[1].GetAvailableFonts().Count);
    Assert.True(newFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));
}
else
{
    Assert.AreEqual(0, newFontSources[1].GetAvailableFonts().Count);
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolders.pdf");

// Stellen Sie die ursprünglichen Schriftartquellen wieder her.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Siehe auch

* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
