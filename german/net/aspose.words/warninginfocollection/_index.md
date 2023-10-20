---
title: WarningInfoCollection Class
linktitle: WarningInfoCollection
articleTitle: WarningInfoCollection
second_title: Aspose.Words für .NET
description: Aspose.Words.WarningInfoCollection klas. Stellt eine typisierte Sammlung von darWarningInfo Objekte in C#.
type: docs
weight: 6640
url: /de/net/aspose.words/warninginfocollection/
---
## WarningInfoCollection class

Stellt eine typisierte Sammlung von dar[`WarningInfo`](../warninginfo/) Objekte.

Um mehr zu erfahren, besuchen Sie die[Programmieren mit Dokumenten](https://docs.aspose.com/words/net/programming-with-documents/) Dokumentationsartikel.

```csharp
public class WarningInfoCollection : IEnumerable<WarningInfo>, IWarningCallback
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [WarningInfoCollection](warninginfocollection/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/warninginfocollection/count/) { get; } | Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab. |
| [Item](../../aspose.words/warninginfocollection/item/) { get; } | Ruft ein Element am angegebenen Index ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clear](../../aspose.words/warninginfocollection/clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [GetEnumerator](../../aspose.words/warninginfocollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, das zum Durchlaufen aller Elemente in der Sammlung verwendet werden kann. |
| [Warning](../../aspose.words/warninginfocollection/warning/)(*[WarningInfo](../warninginfo/)*) | Implementiert die[`IWarningCallback`](../iwarningcallback/) Schnittstelle. Fügt dieser Sammlung eine Warnung hinzu. |

## Bemerkungen

Sie können dieses Sammlungsobjekt als einfachste Form von verwenden[`IWarningCallback`](../iwarningcallback/) Implementierung, um alle Warnungen zu sammeln, die Aspose.Words während eines Lade- oder Speichervorgangs generiert. Erstellen Sie eine Instanz dieser Klasse und weisen Sie sie zu[`WarningCallback`](../../aspose.words.loading/loadoptions/warningcallback/) oder[`WarningCallback`](../documentbase/warningcallback/) Eigentum.

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

* class [WarningInfo](../warninginfo/)
* interface [IWarningCallback](../iwarningcallback/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
