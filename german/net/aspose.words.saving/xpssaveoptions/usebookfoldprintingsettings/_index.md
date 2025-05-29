---
title: XpsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihr Dokumentlayout mit der XpsSaveOptions UseBookFoldPrintingSettings-Eigenschaft und ermöglichen Sie so den nahtlosen Broschürendruck für eine verbesserte Präsentation.
type: docs
weight: 50
url: /de/net/aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/
---
## XpsSaveOptions.UseBookFoldPrintingSettings property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Dokument im Broschüren-Drucklayout gespeichert werden soll, wenn dies über[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Bemerkungen

Wenn diese Option angegeben ist,[`PageSet`](../../fixedpagesaveoptions/pageset/) wird beim Speichern ignoriert. Dieses Verhalten entspricht MS Word. Wenn in der Seiteneinrichtung keine Einstellungen für den Buchfalzdruck angegeben sind, hat diese Option keine Auswirkung.

## Beispiele

Zeigt, wie ein Dokument im XPS-Format in Form einer Buchfalte gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Erstellen Sie ein "XpsSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .XPS konvertiert.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Setzen Sie die Eigenschaft „UseBookFoldPrintingSettings“ auf „true“, um den Inhalt anzuordnen
// im Ausgabe-XPS auf eine Weise, die uns hilft, daraus eine Broschüre zu erstellen.
// Setzen Sie die Eigenschaft „UseBookFoldPrintingSettings“ auf „false“, um das XPS normal zu rendern.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Wenn wir das Dokument als Broschüre rendern, müssen wir die Option "MultiplePages" festlegen.
// Eigenschaften der Seiteneinrichtungsobjekte aller Abschnitte auf „MultiplePagesType.BookFoldPrinting“.
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Sobald wir dieses Dokument drucken, können wir es in eine Broschüre umwandeln, indem wir die Seiten stapeln
// aus dem Drucker kommen und in der Mitte falten.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Siehe auch

* class [XpsSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
