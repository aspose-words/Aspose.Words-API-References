---
title: Document.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die Schrifteinstellungen Ihres Dokuments mühelos anpassen. Verbessern Sie die Lesbarkeit und den Stil Ihrer Dokumente mit maßgeschneiderten Schriftoptionen.
type: docs
weight: 150
url: /de/net/aspose.words/document/fontsettings/
---
## Document.FontSettings property

Ruft die Schriftarteinstellungen des Dokuments ab oder legt sie fest.

```csharp
public FontSettings FontSettings { get; set; }
```

## Bemerkungen

Mit dieser Eigenschaft können Sie Schriftarteinstellungen pro Dokument festlegen. Wenn Sie`null` , statische Standardschrifteinstellungen [`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) verwendet wird.

Der Standardwert ist`null`.

## Beispiele

Zeigt, wie Regeln zum Ersetzen von Schriftarten festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Die Standardschriftartenquellen enthalten die erste Schriftart, die das Dokument verwendet.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Die zweite Schriftart „Amethysta“ ist nicht verfügbar.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Wir können eine Schriftarten-Ersetzungstabelle konfigurieren, die bestimmt
// welche Schriftarten Aspose.Words als Ersatz für nicht verfügbare Schriftarten verwenden wird.
// Legen Sie zwei Ersatzschriftarten für „Amethysta“ fest: „Arvo“ und „Courier New“.
// Wenn der erste Ersatz nicht verfügbar ist, versucht Aspose.Words, den zweiten Ersatz zu verwenden, und so weiter.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

    // „Amethysta“ ist nicht verfügbar und die Ersetzungsregel besagt, dass die erste als Ersatz zu verwendende Schriftart „Arvo“ ist.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

    // „Arvo“ ist ebenfalls nicht verfügbar, „Courier New“ jedoch schon.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Das Ausgabedokument zeigt den Text in der Schriftart „Amethysta“ im Format „Courier New“ an.
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

### Siehe auch

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
