---
title: WarningInfo Class
linktitle: WarningInfo
articleTitle: WarningInfo
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.WarningInfo, die wichtige Einblicke in Warnungen beim Laden oder Speichern von Dokumenten bietet und so die Effizienz Ihres Workflows steigert.
type: docs
weight: 7480
url: /de/net/aspose.words/warninginfo/
---
## WarningInfo class

Enthält Informationen zu einer Warnung, die Aspose.Words beim Laden oder Speichern eines Dokuments ausgegeben hat.

Um mehr zu erfahren, besuchen Sie die[Programmieren mit Dokumenten](https://docs.aspose.com/words/net/programming-with-documents/) Dokumentationsartikel.

```csharp
public class WarningInfo
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Description](../../aspose.words/warninginfo/description/) { get; } | Gibt die Beschreibung der Warnung zurück. |
| [Source](../../aspose.words/warninginfo/source/) { get; } | Gibt die Quelle der Warnung zurück. |
| [WarningType](../../aspose.words/warninginfo/warningtype/) { get; } | Gibt den Typ der Warnung zurück. |

## Bemerkungen

Sie erstellen keine Instanzen dieser Klasse. Objekte dieser Klasse werden erstellt und von Aspose.Words an die[`Warning`](../iwarningcallback/warning/) Verfahren.

## Beispiele

Zeigt, wie die Eigenschaft zum Suchen der besten Entsprechung für eine fehlende Schriftart aus den verfügbaren Schriftartquellen festgelegt wird.

```csharp
public void EnableFontSubstitution()
{
    // Öffnen Sie ein Dokument, das Text enthält, der mit einer Schriftart formatiert ist, die in keiner unserer Schriftartquellen vorhanden ist.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Weisen Sie einen Rückruf für die Behandlung von Warnungen zur Schriftartersetzung zu.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Legen Sie einen Standardschriftnamen fest und aktivieren Sie die Schriftartersetzung.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Nach der Schriftartersetzung sollten die ursprünglichen Schriftmaße verwendet werden.
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

    Assert.AreEqual(0, substitutionWarningHandler.FontWarnings.Count);
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
