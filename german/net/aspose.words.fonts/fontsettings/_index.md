---
title: FontSettings Class
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fonts.FontSettings, um die Schriftarteinstellungen von Dokumenten mühelos anzupassen und so die Lesbarkeit und eine professionelle Präsentation zu verbessern.
type: docs
weight: 3400
url: /de/net/aspose.words.fonts/fontsettings/
---
## FontSettings class

Gibt die Schriftarteinstellungen für ein Dokument an.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Schriftarten](https://docs.aspose.com/words/net/working-with-fonts/) Dokumentationsartikel.

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
| [SubstitutionSettings](../../aspose.words.fonts/fontsettings/substitutionsettings/) { get; } | Einstellungen im Zusammenhang mit dem Schriftartersetzungsmechanismus. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetFontsSources](../../aspose.words.fonts/fontsettings/getfontssources/)() | Ruft eine Kopie des Arrays ab, das die Liste der Quellen enthält, in denen Aspose.Words nach TrueType-Schriftarten sucht. |
| [ResetFontSources](../../aspose.words.fonts/fontsettings/resetfontsources/)() | Setzt die Schriftartenquellen auf die Systemvorgabe zurück. |
| [SaveSearchCache](../../aspose.words.fonts/fontsettings/savesearchcache/)(*Stream*) | Speichert den Schriftartsuchcache im Stream. |
| [SetFontsFolder](../../aspose.words.fonts/fontsettings/setfontsfolder/)(*string, bool*) | Legt den Ordner fest, in dem Aspose.Words beim Rendern von Dokumenten oder beim Einbetten von Schriftarten nach TrueType-Schriftarten sucht. Dies ist eine Verknüpfung zu[`SetFontsFolders`](./setfontsfolders/) zum Einstellen nur eines Schriftartenverzeichnisses. |
| [SetFontsFolders](../../aspose.words.fonts/fontsettings/setfontsfolders/)(*string[], bool*) | Legt die Ordner fest, in denen Aspose.Words beim Rendern von Dokumenten oder beim Einbetten von Schriftarten nach TrueType-Schriftarten sucht. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources)(*FontSourceBase[]*) | Legt die Quellen fest, in denen Aspose.Words beim Rendern von Dokumenten oder beim Einbetten von Schriftarten nach TrueType-Schriftarten sucht. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources_1)(*FontSourceBase[], Stream*) | Legt die Quellen fest, in denen Aspose.Words nach TrueType-Schriftarten sucht und lädt zusätzlich zuvor gespeicherte Schriftartensuch-Cache. |

## Bemerkungen

Aspose.Words verwendet Schrifteinstellungen, um die Schriftarten im Dokument aufzulösen. Die Auflösung erfolgt hauptsächlich beim Erstellen des Dokumentlayouts oder beim Rendern in feste Seitenformate. Beim Laden bestimmter Formate kann Aspose.Words jedoch auch die Auflösung der Schriftarten erfordern. Beispielsweise kann Aspose.Words beim Laden von HTML-Dokumenten die Schriftarten auflösen, um einen Font-Fallback durchzuführen. Es wird daher empfohlen, die Schrifteinstellungen in festzulegen.[`LoadOptions`](../../aspose.words.loading/loadoptions/) beim Laden des Dokuments. Oder zumindest vor dem Erstellen des Layouts oder dem Rendern des Dokuments in das Festseitenformat.

Standardmäßig verwenden alle Dokumente eine einzige statische Schrifteinstellungsinstanz. Der Zugriff erfolgt über [`DefaultInstance`](./defaultinstance/) Eigentum.

Das Ändern der Schrifteinstellungen ist jederzeit und von jedem Thread aus sicher möglich. Es wird jedoch empfohlen, die Schrifteinstellungen nicht zu ändern, während Dokumente verarbeitet werden, die diese Einstellungen verwenden. Dies kann dazu führen, dass dieselbe Schriftart in verschiedenen Teilen des Dokuments unterschiedlich aufgelöst wird.

## Beispiele

Zeigt, wie wir unseren vorhandenen Schriftartquellen eine Schriftartquelle hinzufügen.

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

// In der Standardschriftartquelle fehlen zwei der Schriftarten, die wir in unserem Dokument verwenden.
// Wenn wir dieses Dokument speichern, wendet Aspose.Words Ersatzschriftarten auf den gesamten Text an, der mit nicht zugänglichen Schriftarten formatiert ist.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Erstellen Sie eine Schriftartquelle aus einem Ordner, der Schriftarten enthält.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Wenden Sie ein neues Array von Schriftartquellen an, das die ursprünglichen Schriftartquellen sowie unsere benutzerdefinierten Schriftarten enthält.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Überprüfen Sie, ob Aspose.Words Zugriff auf alle erforderlichen Schriftarten hat, bevor wir das Dokument in PDF rendern.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Stellen Sie die ursprünglichen Schriftartquellen wieder her.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

Zeigt, wie ein Schriftartquellenverzeichnis festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Unsere Schriftartquellen enthalten nicht die Schriftart, die wir für den Text in diesem Dokument verwendet haben.
// Wenn wir diese Schrifteinstellungen beim Rendern dieses Dokuments verwenden,
// Aspose.Words wendet eine Ersatzschriftart auf Text an, der eine Schriftart enthält, die Aspose.Words nicht finden kann.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// In den Standardschriftartenquellen fehlen die beiden Schriftarten, die wir in diesem Dokument verwenden.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Verwenden Sie die Methode „SetFontsFolder“, um ein Verzeichnis festzulegen, das als neue Schriftartquelle fungiert.
// Übergeben Sie "false" als "rekursives" Argument, um Schriftarten aus allen Schriftartdateien einzuschließen, die sich im Verzeichnis befinden
// dass wir das erste Argument übergeben, aber keine Schriftarten in den Unterordnern dieses Verzeichnisses einschließen.
// Übergeben Sie "true" als "rekursives" Argument, um alle Schriftdateien im Verzeichnis einzuschließen, das wir übergeben
// im ersten Argument sowie alle Schriftarten in seinen Unterverzeichnissen.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Die Schriftart „Amethysta“ befindet sich in einem Unterordner des Schriftartenverzeichnisses.
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

Zeigt, wie mehrere Schriftartquellenverzeichnisse festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Unsere Schriftartquellen enthalten nicht die Schriftart, die wir für den Text in diesem Dokument verwendet haben.
// Wenn wir diese Schrifteinstellungen beim Rendern dieses Dokuments verwenden,
// Aspose.Words wendet eine Ersatzschriftart auf Text an, der eine Schriftart enthält, die Aspose.Words nicht finden kann.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// In den Standardschriftartenquellen fehlen die beiden Schriftarten, die wir in diesem Dokument verwenden.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Verwenden Sie die Methode „SetFontsFolders“, um aus jedem Schriftartenverzeichnis, das wir als erstes Argument übergeben, eine Schriftartenquelle zu erstellen.
// Übergeben Sie "false" als "rekursives" Argument, um Schriftarten aus allen Schriftartdateien einzuschließen, die sich in den Verzeichnissen befinden
// die wir im ersten Argument übergeben, aber keine Schriftarten aus den Unterordnern der Verzeichnisse einschließen.
// Übergeben Sie "true" als "rekursives" Argument, um alle Schriftdateien in den Verzeichnissen einzuschließen, die wir übergeben
// im ersten Argument sowie alle Schriftarten in ihren Unterverzeichnissen.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Der Ordner „Junction“ selbst enthält keine Schriftdateien, hat aber Unterordner, die welche enthalten.
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
