---
title: PageSetup.SheetsPerBooklet
linktitle: SheetsPerBooklet
articleTitle: SheetsPerBooklet
second_title: Aspose.Words für .NET
description: PageSetup SheetsPerBooklet eigendom. Gibt die Anzahl der Seiten zurück die in jede Broschüre aufgenommen werden sollen oder legt sie fest in C#.
type: docs
weight: 400
url: /de/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

Gibt die Anzahl der Seiten zurück, die in jede Broschüre aufgenommen werden sollen, oder legt sie fest.

```csharp
public int SheetsPerBooklet { get; set; }
```

## Beispiele

Zeigt, wie ein Dokument konfiguriert wird, das als Buchfalte gedruckt werden kann.

```csharp
Document doc = new Document();

// Text einfügen, der 16 Seiten umfasst.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Konfigurieren Sie die Eigenschaft „PageSetup“ des ersten Abschnitts, um das Dokument in Form einer Buchfalte zu drucken.
// Wenn wir dieses Dokument auf beiden Seiten drucken, können wir die Seiten zum Stapeln verwenden
// und alle auf einmal in der Mitte falten. Der Inhalt des Dokuments wird in einer Buchfalte angeordnet.
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
