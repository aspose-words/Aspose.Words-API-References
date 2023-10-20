---
title: PsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words für .NET
description: PsSaveOptions UseBookFoldPrintingSettings eigendom. Ruft einen booleschen Wert ab oder legt diesen fest der angibt ob das Dokument mit einem Broschürendrucklayout gespeichert werden soll  wenn es über angegeben wirdMultiplePages  in C#.
type: docs
weight: 30
url: /de/net/aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/
---
## PsSaveOptions.UseBookFoldPrintingSettings property

Ruft einen booleschen Wert ab oder legt diesen fest, der angibt, ob das Dokument mit einem Broschürendrucklayout gespeichert werden soll, , wenn es über angegeben wird[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Bemerkungen

Wenn diese Option angegeben ist,[`PageSet`](../../fixedpagesaveoptions/pageset/) wird beim Speichern ignoriert. Dieses Verhalten entspricht MS Word. Wenn in der Seiteneinrichtung keine Buchfaltdruckeinstellungen angegeben sind, hat diese Option keine Auswirkung.

## Beispiele

Zeigt, wie ein Dokument im Postscript-Format in Form einer Buchfalte gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Erstellen Sie ein „PsSaveOptions“-Objekt, das wir an die „Save“-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in PostScript konvertiert.
// Setzen Sie die Eigenschaft „UseBookFoldPrintingSettings“ auf „true“, um den Inhalt anzuordnen
// im ausgegebenen Postscript-Dokument auf eine Weise einfügen, die uns hilft, daraus eine Broschüre zu erstellen.
// Setzen Sie die Eigenschaft „UseBookFoldPrintingSettings“ auf „false“, um das Dokument normal zu speichern.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Wenn wir das Dokument als Broschüre rendern, müssen wir „MultiplePages“ festlegen.
// Eigenschaften der Seiteneinrichtungsobjekte aller Abschnitte zu „MultiplePagesType.BookFoldPrinting“.
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// Sobald wir dieses Dokument auf beiden Seiten der Seiten drucken, können wir alle Seiten auf einmal in der Mitte falten.
// und der Inhalt wird so ausgerichtet, dass eine Broschüre entsteht.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Siehe auch

* class [PsSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
