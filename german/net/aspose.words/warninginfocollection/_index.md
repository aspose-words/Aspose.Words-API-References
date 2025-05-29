---
title: WarningInfoCollection Class
linktitle: WarningInfoCollection
articleTitle: WarningInfoCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.WarningInfoCollection, eine leistungsstarke Klasse zum Verwalten von WarningInfo-Objekten, die die Dokumentverarbeitung und Fehlerbehandlung verbessert.
type: docs
weight: 7490
url: /de/net/aspose.words/warninginfocollection/
---
## WarningInfoCollection class

Stellt eine typisierte Sammlung von[`WarningInfo`](../warninginfo/) Objekte.

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
| [GetEnumerator](../../aspose.words/warninginfocollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, mit dem alle Elemente in der Sammlung durchlaufen werden können. |
| [Warning](../../aspose.words/warninginfocollection/warning/)(*[WarningInfo](../warninginfo/)*) | Implementiert die[`IWarningCallback`](../iwarningcallback/) Schnittstelle. Fügt dieser Sammlung eine Warnung hinzu. |

## Bemerkungen

Sie können dieses Sammlungsobjekt als einfachste Form von[`IWarningCallback`](../iwarningcallback/) Implementierung, um alle Warnungen zu erfassen, die Aspose.Words während eines Lade- oder Speichervorgangs generiert. Erstellen Sie eine Instanz dieser Klasse und weisen Sie sie dem[`WarningCallback`](../../aspose.words.loading/loadoptions/warningcallback/) oder[`WarningCallback`](../documentbase/warningcallback/) Eigentum.

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

* class [WarningInfo](../warninginfo/)
* interface [IWarningCallback](../iwarningcallback/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
