---
title: XpsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words für .NET
description: XpsSaveOptions UseBookFoldPrintingSettings eigendom. Ruft einen booleschen Wert ab oder legt diesen fest der angibt ob das Dokument mit einem Broschürendrucklayout gespeichert werden soll  wenn es über angegeben wirdMultiplePages  in C#.
type: docs
weight: 40
url: /de/net/aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/
---
## XpsSaveOptions.UseBookFoldPrintingSettings property

Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, ob das Dokument mit einem Broschürendrucklayout gespeichert werden soll, , wenn es über angegeben wird[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Bemerkungen

Wenn diese Option angegeben ist,[`PageSet`](../../fixedpagesaveoptions/pageset/) wird beim Speichern ignoriert. Dieses Verhalten entspricht MS Word. Wenn in der Seiteneinrichtung keine Buchfaltdruckeinstellungen angegeben sind, hat diese Option keine Auswirkung.

## Beispiele

Zeigt, wie ein Dokument in Form einer Buchfalte im XPS-Format gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Erstellen Sie ein „XpsSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .XPS konvertiert.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Setzen Sie die Eigenschaft „UseBookFoldPrintingSettings“ auf „true“, um den Inhalt anzuordnen
// im Ausgabe-XPS auf eine Weise, die uns hilft, daraus eine Broschüre zu erstellen.
// Setzen Sie die Eigenschaft „UseBookFoldPrintingSettings“ auf „false“, um das XPS normal darzustellen.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Wenn wir das Dokument als Broschüre rendern, müssen wir „MultiplePages“ festlegen.
// Eigenschaften der Seiteneinrichtungsobjekte aller Abschnitte zu „MultiplePagesType.BookFoldPrinting“.
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Sobald wir dieses Dokument gedruckt haben, können wir es durch Stapeln der Seiten in eine Broschüre umwandeln
// aus dem Drucker kommen und in der Mitte nach unten falten.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Siehe auch

* class [XpsSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
