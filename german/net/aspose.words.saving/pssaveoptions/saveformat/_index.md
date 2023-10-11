---
title: PsSaveOptions.SaveFormat
second_title: Aspose.Words für .NET-API-Referenz
description: PsSaveOptions eigendom. Gibt das Format an in dem das Dokument gespeichert wird wenn dieses Speicheroptionsobjekt verwendet wird. Kann nur seinPs .
type: docs
weight: 20
url: /de/net/aspose.words.saving/pssaveoptions/saveformat/
---
## PsSaveOptions.SaveFormat property

Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann nur seinPs .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Beispiele

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PsSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../pssaveoptions/)
* Montage [Aspose.Words](../../../)


