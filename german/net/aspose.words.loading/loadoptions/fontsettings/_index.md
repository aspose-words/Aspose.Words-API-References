---
title: LoadOptions.FontSettings
second_title: Aspose.Words für .NET-API-Referenz
description: LoadOptions eigendom. Ermöglicht das Festlegen von Schriftarteinstellungen für Dokumente.
type: docs
weight: 60
url: /de/net/aspose.words.loading/loadoptions/fontsettings/
---
## LoadOptions.FontSettings property

Ermöglicht das Festlegen von Schriftarteinstellungen für Dokumente.

```csharp
public FontSettings FontSettings { get; set; }
```

### Bemerkungen

Beim Laden einiger Formate muss Aspose.Words möglicherweise die Schriftarten auflösen. Beim Laden von HTML-Dokumenten kann Aspose.Words beispielsweise die Schriftarten auflösen, um einen Schriftart-Fallback durchzuführen.

Wenn eingestellt auf`Null` , Standardeinstellungen für statische Schriftarten[`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) verwendet wird.

Der Standardwert ist`Null`.

### Beispiele

Zeigt, wie Schriftartersetzungseinstellungen beim Laden eines Dokuments angewendet werden.

```csharp
// Erstellen Sie ein FontSettings-Objekt, das die Schriftart „Times New Roman“ ersetzt
// mit der Schriftart „Arvo“ aus unserem „MyFonts“-Ordner.
FontSettings fontSettings = new FontSettings();
fontSettings.SetFontsFolder(FontsDir, false);
fontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Times New Roman", "Arvo");

// Dieses FontSettings-Objekt als Eigenschaft eines neu erstellten LoadOptions-Objekts festlegen.
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = fontSettings;

// Laden Sie das Dokument und rendern Sie es dann als PDF mit der Schriftartersetzung.
Document doc = new Document(MyDir + "Document.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.FontSettings.pdf");
```

Zeigt, wie Schriftartersatz beim Laden festgelegt wird.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = new FontSettings();

// Legen Sie eine Schriftartersetzungsregel für ein LoadOptions-Objekt fest.
// Wenn das Dokument, das wir laden, eine Schriftart verwendet, die wir nicht haben,
// Diese Regel ersetzt die nicht verfügbare Schriftart durch eine vorhandene.
// In diesem Fall werden alle Verwendungen von „MissingFont“ in „Comic Sans MS“ konvertiert.
TableSubstitutionRule substitutionRule = loadOptions.FontSettings.SubstitutionSettings.TableSubstitution;
substitutionRule.AddSubstitutes("MissingFont", new[] {"Comic Sans MS"});

Document doc = new Document(MyDir + "Missing font.html", loadOptions);

// Zu diesem Zeitpunkt befindet sich dieser Text immer noch in „MissingFont“.
// Die Schriftartenersetzung findet statt, wenn wir das Dokument rendern.
Assert.AreEqual("MissingFont", doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Name);

doc.Save(ArtifactsDir + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```

### Siehe auch

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../loadoptions/)
* Montage [Aspose.Words](../../../)


