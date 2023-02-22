---
title: Enum WarningType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.WarningType opsomming. Gibt den Typ einer Warnung an die von Aspose.Words beim Laden oder Speichern von Dokumenten ausgegeben wird.
type: docs
weight: 6350
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
| DataLossCategory | `FF` | Einige Text-/Zeichen-/Bild- oder andere Daten fehlen entweder im Dokumentbaum nach dem Laden oder im erstellten Dokument nach dem Speichern. |
| DataLoss | `1` | Allgemeiner Datenverlust, kein spezifischer Code. |
| MajorFormattingLossCategory | `FF00` | Das resultierende Dokument oder eine bestimmte Stelle darin kann im Vergleich zum Originaldokument erheblich anders aussehen. |
| MajorFormattingLoss | `100` | Allgemeiner großer Formatierungsverlust, kein spezifischer Code. |
| MinorFormattingLossCategory | `FF0000` | Das resultierende Dokument oder eine bestimmte Stelle darin kann im Vergleich zum Originaldokument etwas anders aussehen. |
| MinorFormattingLoss | `10000` | Allgemeiner geringfügiger Formatierungsverlust, kein spezifischer Code. |
| FontSubstitution | `20000` | Schriftart wurde ersetzt. |
| FontEmbedding | `40000` | Verlust eingebetteter Schriftinformationen beim Speichern des Dokuments. |
| UnexpectedContentCategory | `F000000` | Einige Inhalte im Quelldokument konnten nicht erkannt werden (dh werden nicht unterstützt), dies kann oder kann nicht Probleme verursachen oder zu Daten-/Formatierungsverlust führen. |
| UnexpectedContent | `1000000` | Allgemeiner unerwarteter Inhalt, kein spezifischer Code. |
| Hint | `10000000` | Weist auf ein potenzielles Problem hin oder schlägt eine Verbesserung vor. |

### Beispiele

Zeigt, wie die Eigenschaft festgelegt wird, um die beste Übereinstimmung für eine fehlende Schriftart aus den verfügbaren Schriftartquellen zu finden.

```csharp
[Test]
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

    // Wir erhalten eine Schriftersetzungswarnung, wenn wir ein Dokument mit einer fehlenden Schrift speichern.
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
    /// Wird jedes Mal aufgerufen, wenn während des Ladens/Speicherns eine Warnung auftritt.
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


