---
title: PsSaveOptions.UseBookFoldPrintingSettings
second_title: Aspose.Words für .NET-API-Referenz
description: PsSaveOptions eigendom. Erhält oder setzt einen booleschen Wert der angibt ob das Dokument mit einem Broschürendrucklayout gespeichert werden soll  wenn dies über angegeben wirdMultiplePages .
type: docs
weight: 30
url: /de/net/aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/
---
## PsSaveOptions.UseBookFoldPrintingSettings property

Erhält oder setzt einen booleschen Wert, der angibt, ob das Dokument mit einem Broschürendrucklayout gespeichert werden soll, , wenn dies über angegeben wird[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

### Bemerkungen

Wenn diese Option angegeben ist,[`PageSet`](../../fixedpagesaveoptions/pageset/) wird beim Speichern ignoriert. Dieses Verhalten entspricht MS Word. Wenn in der Seiteneinrichtung keine Buchfalzdruckeinstellungen angegeben sind, hat diese Option keine Auswirkung.

### Beispiele

Zeigt, wie ein Dokument im Postscript-Format in Form einer Buchfaltung gespeichert wird.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Erstellen Sie ein "PsSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in PostScript konvertiert.
// Setzen Sie die Eigenschaft "UseBookFoldPrintingSettings" auf "true", um den Inhalt anzuordnen
// im ausgegebenen Postscript-Dokument auf eine Weise, die uns hilft, eine Broschüre daraus zu machen.
// Setzen Sie die Eigenschaft "UseBookFoldPrintingSettings" auf "false", um das Dokument normal zu speichern.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Wenn wir das Dokument als Booklet rendern, müssen wir "MultiplePages" setzen
// Eigenschaften der Seiteneinrichtungsobjekte aller Abschnitte auf "MultiplePagesType.BookFoldPrinting".
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// Sobald wir dieses Dokument auf beiden Seiten der Seiten drucken, können wir alle Seiten auf einmal in der Mitte falten,
// und der Inhalt wird so ausgerichtet, dass eine Broschüre entsteht.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Siehe auch

* class [PsSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../pssaveoptions/)
* Montage [Aspose.Words](../../../)


