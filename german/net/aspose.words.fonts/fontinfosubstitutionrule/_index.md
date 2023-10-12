---
title: Class FontInfoSubstitutionRule
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Fonts.FontInfoSubstitutionRule klas. SchriftartInfoErsetzungsregel.
type: docs
weight: 2940
url: /de/net/aspose.words.fonts/fontinfosubstitutionrule/
---
## FontInfoSubstitutionRule class

Schriftart-Info-Ersetzungsregel.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Schriftarten](https://docs.aspose.com/words/net/working-with-fonts/) Dokumentationsartikel.

```csharp
public class FontInfoSubstitutionRule : FontSubstitutionRule
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Gibt an, ob die Regel aktiviert ist oder nicht. |

### Bemerkungen

Gemäß dieser Regel wertet Aspose.Words alle zugehörigen Felder in aus[`FontInfo`](../fontinfo/) (Panose, Sig usw.) for die fehlende Schriftart und findet die beste Übereinstimmung unter den verfügbaren Schriftartquellen. Wenn[`FontInfo`](../fontinfo/)Ist die fehlende Schriftart nicht verfügbar, wird nichts unternommen.

### Beispiele

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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* namensraum [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Montage [Aspose.Words](../../)


