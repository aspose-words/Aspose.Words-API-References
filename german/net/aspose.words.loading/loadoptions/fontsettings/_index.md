---
title: LoadOptions.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words für .NET
description: Passen Sie die Schrifteinstellungen Ihres Dokuments mit LoadOptions FontSettings an, um Lesbarkeit und Stil zu verbessern. Optimieren Sie Ihre Dokumente mühelos!
type: docs
weight: 60
url: /de/net/aspose.words.loading/loadoptions/fontsettings/
---
## LoadOptions.FontSettings property

Ermöglicht die Festlegung von Schriftarteinstellungen für Dokumente.

```csharp
public FontSettings FontSettings { get; set; }
```

## Bemerkungen

Beim Laden einiger Formate muss Aspose.Words möglicherweise die Schriftarten auflösen. Beispielsweise kann Aspose.Words beim Laden von HTML-Dokumenten die Schriftarten auflösen, um einen Font-Fallback durchzuführen.

Wenn eingestellt auf`null` , statische Standardschrifteinstellungen[`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) verwendet wird.

Der Standardwert ist`null`.

## Beispiele

Zeigt, wie Sie beim Laden eines Dokuments Einstellungen zur Schriftartersetzung anwenden.

```csharp
// Erstellen Sie ein FontSettings-Objekt, das die Schriftart „Times New Roman“ ersetzt
// mit der Schriftart „Arvo“ aus unserem Ordner „MyFonts“.
FontSettings fontSettings = new FontSettings();
fontSettings.SetFontsFolder(FontsDir, false);
fontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Times New Roman", "Arvo");

// Legen Sie dieses FontSettings-Objekt als Eigenschaft eines neu erstellten LoadOptions-Objekts fest.
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = fontSettings;

// Laden Sie das Dokument und rendern Sie es dann mit der Schriftartersetzung als PDF.
Document doc = new Document(MyDir + "Document.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.FontSettings.pdf");
```

Zeigt, wie beim Laden Schriftartenersatz festgelegt wird.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = new FontSettings();

// Legen Sie eine Schriftartersetzungsregel für ein LoadOptions-Objekt fest.
// Wenn das Dokument, das wir laden, eine Schriftart verwendet, die wir nicht haben,
// Diese Regel ersetzt die nicht verfügbare Schriftart durch eine vorhandene.
// In diesem Fall werden alle Verwendungen von „MissingFont“ in „Comic Sans MS“ konvertiert.
TableSubstitutionRule substitutionRule = loadOptions.FontSettings.SubstitutionSettings.TableSubstitution;
substitutionRule.AddSubstitutes("MissingFont", "Comic Sans MS");

Document doc = new Document(MyDir + "Missing font.html", loadOptions);

// An dieser Stelle wird der Text noch immer in „MissingFont“ angezeigt.
// Die Schriftartersetzung erfolgt beim Rendern des Dokuments.
Assert.AreEqual("MissingFont", doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Name);

doc.Save(ArtifactsDir + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```

### Siehe auch

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
