---
title: PsSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die SaveFormat-Eigenschaft von PsSaveOptions, um das Speicherformat Ihres Dokuments einfach festzulegen. Optimieren Sie Ihren Workflow mit flexiblen Speicheroptionen!
type: docs
weight: 20
url: /de/net/aspose.words.saving/pssaveoptions/saveformat/
---
## PsSaveOptions.SaveFormat property

Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann nurPs .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PsSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
