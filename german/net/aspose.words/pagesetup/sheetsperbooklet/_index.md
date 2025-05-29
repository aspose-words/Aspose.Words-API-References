---
title: PageSetup.SheetsPerBooklet
linktitle: SheetsPerBooklet
articleTitle: SheetsPerBooklet
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „PageSetup SheetsPerBooklet“, um die Seitenanzahl von Broschüren einfach zu verwalten und so Ihr Dokumentenlayout und Ihre Druckeffizienz zu verbessern.
type: docs
weight: 400
url: /de/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

Gibt die Anzahl der Seiten zurück, die in jeder Broschüre enthalten sein sollen, oder legt sie fest.

```csharp
public int SheetsPerBooklet { get; set; }
```

## Beispiele

Zeigt, wie ein Dokument konfiguriert wird, das als Buchfalz gedruckt werden kann.

```csharp
Document doc = new Document();

// Text einfügen, der sich über 16 Seiten erstreckt.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Konfigurieren Sie die Eigenschaft „PageSetup“ des ersten Abschnitts, um das Dokument in Form einer Buchfalte zu drucken.
// Wenn wir dieses Dokument beidseitig drucken, können wir die Seiten nehmen, um sie zu stapeln
// und falten Sie sie alle gleichzeitig in der Mitte. Der Inhalt des Dokuments wird in einer Buchfalte ausgerichtet.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Wir können die Anzahl der Blätter nur in Vielfachen von 4 angeben.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
