---
title: TextColumnCollection Class
linktitle: TextColumnCollection
articleTitle: TextColumnCollection
second_title: Aspose.Words für .NET
description: Erkunden Sie Aspose.Words.TextColumnCollection, um Textspalten in Ihren Dokumenten mühelos zu verwalten. Verbessern Sie die Formatierung Ihrer Dokumente mit Leichtigkeit!
type: docs
weight: 7250
url: /de/net/aspose.words/textcolumncollection/
---
## TextColumnCollection class

Eine Sammlung von[`TextColumn`](../textcolumn/) Objekte, die alle Textspalten in einem Abschnitt eines Dokuments darstellen.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Abschnitten](https://docs.aspose.com/words/net/working-with-sections/) Dokumentationsartikel.

```csharp
public class TextColumnCollection
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/textcolumncollection/count/) { get; } | Ruft die Anzahl der Spalten im Abschnitt eines Dokuments ab. |
| [EvenlySpaced](../../aspose.words/textcolumncollection/evenlyspaced/) { get; set; } | Wahr, wenn die Textspalten gleich breit und gleichmäßig verteilt sind. |
| [Item](../../aspose.words/textcolumncollection/item/) { get; } | Gibt eine Textspalte am angegebenen Index zurück. |
| [LineBetween](../../aspose.words/textcolumncollection/linebetween/) { get; set; } | Wann`WAHR` , fügt eine vertikale Linie zwischen den Spalten hinzu. |
| [Spacing](../../aspose.words/textcolumncollection/spacing/) { get; set; } | Wenn die Spalten gleichmäßig verteilt sind, wird der Abstand zwischen den einzelnen Spalten in Punkten abgerufen oder festgelegt. |
| [Width](../../aspose.words/textcolumncollection/width/) { get; } | Wenn die Spalten gleichmäßig verteilt sind, wird die Breite der Spalten abgerufen. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [SetCount](../../aspose.words/textcolumncollection/setcount/)(*int*) | Ordnet Text in die angegebene Anzahl von Textspalten an. |

## Bemerkungen

Verwenden[`SetCount`](./setcount/) um die Anzahl der Textspalten festzulegen.

Um alle Spalten gleich breit und gleichmäßig zu verteilen, setzen Sie[`EvenlySpaced`](./evenlyspaced/) Zu`WAHR` und geben Sie den Abstand zwischen den Spalten in[`Spacing`](./spacing/). MS Word berechnet die Spaltenbreiten automatisch.

Wenn Sie[`EvenlySpaced`](./evenlyspaced/) eingestellt auf`FALSCH` müssen Sie Breite und Abstand für jede -Spalte einzeln angeben. Verwenden Sie den Indexer, um auf einzelne[`TextColumn`](../textcolumn/) Objekte.

Wenn Sie benutzerdefinierte Spaltenbreiten verwenden, stellen Sie sicher, dass die Summe aller Spaltenbreiten und Abstände zwischen ihnen der Seitenbreite abzüglich der linken und rechten Seitenränder entspricht.

## Beispiele

Zeigt, wie mehrere gleichmäßig verteilte Spalten in einem Abschnitt erstellt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
