---
title: MultiplePagesType Enum
linktitle: MultiplePagesType
articleTitle: MultiplePagesType
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.Settings.MultiplePagesType für effiziente Dokumentdruckoptionen. Optimieren Sie Ihren Workflow mit flexiblen Druckeinstellungen!
type: docs
weight: 6700
url: /de/net/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enumeration

Gibt an, wie das Dokument ausgedruckt wird.

```csharp
public enum MultiplePagesType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Normal | `0` | Normaler Druck, keine Angabe mehrerer Seiten. |
| MirrorMargins | `1` | Vertauscht den linken und rechten Rand auf gegenüberliegenden Seiten. |
| TwoPagesPerSheet | `2` | Druckt zwei Seiten pro Blatt. |
| BookFoldPrinting | `3` | Gibt an, ob das Dokument als Buchfalz gedruckt werden soll. |
| BookFoldPrintingReverse | `4` | Gibt an, ob das Dokument als umgekehrte Buchfalz gedruckt werden soll. |
| Default | `0` | Der Standardwert istNormal |

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

* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)
