---
title: PsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „PsSaveOptions UseBookFoldPrintingSettings“, um Dokumente einfach in einem Broschürenlayout zu speichern und so die Druckeffizienz zu verbessern.
type: docs
weight: 30
url: /de/net/aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/
---
## PsSaveOptions.UseBookFoldPrintingSettings property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Dokument im Broschüren-Drucklayout gespeichert werden soll, wenn dies über[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Bemerkungen

Wenn diese Option angegeben ist,[`PageSet`](../../fixedpagesaveoptions/pageset/) wird beim Speichern ignoriert. Dieses Verhalten entspricht MS Word. Wenn in der Seiteneinrichtung keine Einstellungen für den Buchfalzdruck angegeben sind, hat diese Option keine Auswirkung.

## Beispiele

Zeigt, wie ein Dokument im Postscript-Format in Form einer Buchfalte gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Erstellen Sie ein "PsSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in PostScript konvertiert.
// Setzen Sie die Eigenschaft „UseBookFoldPrintingSettings“ auf „true“, um den Inhalt anzuordnen
// im Postscript-Ausgabedokument auf eine Weise, die uns hilft, eine Broschüre daraus zu machen.
// Setzen Sie die Eigenschaft „UseBookFoldPrintingSettings“ auf „false“, um das Dokument normal zu speichern.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Wenn wir das Dokument als Broschüre rendern, müssen wir die Option "MultiplePages" festlegen.
// Eigenschaften der Seiteneinrichtungsobjekte aller Abschnitte auf „MultiplePagesType.BookFoldPrinting“.
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// Sobald wir dieses Dokument beidseitig bedruckt haben, können wir alle Seiten gleichzeitig in der Mitte falten.
// und die Inhalte werden so angeordnet, dass eine Broschüre entsteht.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Siehe auch

* class [PsSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
