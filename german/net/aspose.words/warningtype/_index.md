---
title: WarningType Enum
linktitle: WarningType
articleTitle: WarningType
second_title: Aspose.Words für .NET
description: Aspose.Words.WarningType opsomming. Gibt den Typ einer Warnung an die von Aspose.Words beim Laden oder Speichern von Dokumenten ausgegeben wird in C#.
type: docs
weight: 6660
url: /de/net/aspose.words/warningtype/
---
## WarningType enumeration

Gibt den Typ einer Warnung an, die von Aspose.Words beim Laden oder Speichern von Dokumenten ausgegeben wird.

```csharp
[Flags]
public enum WarningType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| DataLossCategory | `FF` | Einige Text-, Zeichen-, Bild- oder andere Daten fehlen entweder im Dokumentbaum nach dem Laden, oder im erstellten Dokument nach dem Speichern. |
| DataLoss | `1` | Allgemeiner Datenverlust, kein spezifischer Code. |
| MajorFormattingLossCategory | `FF00` | Das resultierende Dokument oder eine bestimmte Stelle darin sieht möglicherweise erheblich anders aus als das Originaldokument. |
| MajorFormattingLoss | `100` | Generell schwerwiegender Formatierungsverlust, kein spezifischer Code. |
| MinorFormattingLossCategory | `FF0000` | Das resultierende Dokument oder eine bestimmte Stelle darin sieht im Vergleich möglicherweise etwas anders aus als das Originaldokument. |
| MinorFormattingLoss | `10000` | Allgemeiner geringfügiger Formatierungsverlust, kein spezifischer Code. |
| FontSubstitution | `20000` | Schriftart wurde ersetzt. |
| FontEmbedding | `40000` | Verlust eingebetteter Schriftartinformationen beim Speichern des Dokuments. |
| UnexpectedContentCategory | `F000000` | Einige Inhalte im Quelldokument konnten nicht erkannt werden (d. h. werden nicht unterstützt). Dies kann zu Problemen führen oder zu Daten-/Formatierungsverlusten führen. |
| UnexpectedContent | `1000000` | Allgemeiner unerwarteter Inhalt, kein spezifischer Code. |
| Hint | `10000000` | Macht auf ein potenzielles Problem aufmerksam oder schlägt eine Verbesserung vor. |

## Beispiele

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

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
