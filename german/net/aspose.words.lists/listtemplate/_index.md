---
title: ListTemplate Enum
linktitle: ListTemplate
articleTitle: ListTemplate
second_title: Aspose.Words für .NET
description: Aspose.Words.Lists.ListTemplate opsomming. Gibt eines der vordefinierten Listenformate an die in Microsoft Word verfügbar sind in C#.
type: docs
weight: 3530
url: /de/net/aspose.words.lists/listtemplate/
---
## ListTemplate enumeration

Gibt eines der vordefinierten Listenformate an, die in Microsoft Word verfügbar sind.

```csharp
public enum ListTemplate
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| BulletDefault | `0` | Standardliste mit Aufzählungszeichen und 9 Ebenen. Aufzählungszeichen der ersten Ebene ist eine Scheibe, Aufzählungszeichen der zweiten Ebene ist ein Kreis, Aufzählungszeichen der dritten Ebene ist ein Quadrat. Anschließend wird die Formatierung für die verbleibenden Ebenen wiederholt. |
| BulletDisk | `0` | Gleich wieBulletDefault. |
| BulletCircle | `1` | Die Kugel der ersten Ebene ist ein Kreis. Die übrigen Level sind die gleichen wie inBulletDefault. |
| BulletSquare | `2` | Die Kugel der ersten Ebene ist ein Quadrat. Die übrigen Level sind die gleichen wie inBulletDefault. |
| BulletDiamonds | `3` | Die Kugel des ersten Levels ist ein 4-Diamanten-Wingding-Charakter. Die übrigen Level sind die gleichen wie inBulletDefault. |
| BulletArrowHead | `4` | Die Kugel des ersten Levels ist ein Wingding-Charakter mit Pfeilspitze. Die übrigen Level sind die gleichen wie inBulletDefault. |
| BulletTick | `5` | Die Kugel des ersten Levels ist ein Tick-Wingding-Charakter. Die übrigen Level sind die gleichen wie inBulletDefault. |
| NumberDefault | `6` | Standardmäßig nummerierte Liste mit 9 Ebenen. Arabische Nummerierung (1., 2., 3., ...) für die erste Ebene, Nummerierung in Kleinbuchstaben (a., b., c., ...) für die zweite Ebene, Nummerierung in Kleinbuchstaben in römischer Schrift (i ., ii., iii., ...) für die dritte Ebene. Anschließend wird die Formatierung für die verbleibenden Ebenen wiederholt. |
| NumberArabicDot | `6` | Gleich wieNumberDefault. |
| NumberArabicParenthesis | `7` | Die Nummer der ersten Ebene ist „1)“. Die übrigen Level sind die gleichen wie inNumberDefault. |
| NumberUppercaseRomanDot | `8` | Die Nummer der ersten Ebene ist „I.“ Die übrigen Level sind die gleichen wie inNumberDefault. |
| NumberUppercaseLetterDot | `9` | Die Nummer der ersten Ebene ist „A.“ Die übrigen Level sind die gleichen wie inNumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | Die Nummer der ersten Ebene ist „a)“. Die übrigen Level sind die gleichen wie inNumberDefault. |
| NumberLowercaseLetterDot | `11` | Die Nummer der ersten Ebene ist „a.“ Die übrigen Level sind die gleichen wie inNumberDefault. |
| NumberLowercaseRomanDot | `12` | Die Nummer der ersten Ebene ist „i.“ Die übrigen Level sind die gleichen wie inNumberDefault. |
| OutlineNumbers | `13` | Eine Übersichtsliste mit den Ebenen nummeriert „1), a), i), (1), (a), (i), 1., a., i.“ |
| OutlineLegal | `14` | Eine Übersichtsliste mit Ebenen ist mit „1., 1.1., 1.1.1, ...“ nummeriert. |
| OutlineBullets | `15` | Eine Übersichtsliste mit verschiedenen Aufzählungszeichen für verschiedene Ebenen. |
| OutlineHeadingsArticleSection | `16` | Eine Gliederungsliste mit Ebenen, die mit Überschriftenstilen verknüpft sind. |
| OutlineHeadingsLegal | `17` | Eine Gliederungsliste mit Ebenen, die mit Überschriftenstilen verknüpft sind. |
| OutlineHeadingsNumbers | `18` | Eine Gliederungsliste mit Ebenen, die mit Überschriftenstilen verknüpft sind. |
| OutlineHeadingsChapter | `19` | Eine Gliederungsliste mit Ebenen, die mit Überschriftenstilen verknüpft sind. |

## Bemerkungen

Ein Listenvorlagenwert wird als Parameter in the verwendet.[`Add`](../listcollection/add/) Methode.

Aspose.Words-Listenvorlagen entsprechen den 21 verfügbaren Listenvorlagen im Dialogfeld „Aufzählungszeichen und Nummerierung“ in Microsoft Word 2003.

## Beispiele

Zeigt, wie ein Dokument erstellt wird, das alle Listenvorlagen für Gliederungsüberschriften enthält.

```csharp
public void OutlineHeadingTemplates()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    List list = doc.Lists.Add(ListTemplate.OutlineHeadingsArticleSection);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Article Section\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsLegal);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Legal\"");

    builder.InsertBreak(BreakType.PageBreak);

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsNumbers);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Numbers\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsChapter);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Chapters\"");

    doc.Save(ArtifactsDir + "Lists.OutlineHeadingTemplates.docx");
}

private static void AddOutlineHeadingParagraphs(DocumentBuilder builder, List list, string title)
{
    builder.ParagraphFormat.ClearFormatting();
    builder.Writeln(title);

    for (int i = 0; i < 9; i++)
    {
        builder.ListFormat.List = list;
        builder.ListFormat.ListLevelNumber = i;

        string styleName = "Heading " + (i + 1);
        builder.ParagraphFormat.StyleName = styleName;
        builder.Writeln(styleName);
    }

    builder.ListFormat.RemoveNumbers();
}
```

Zeigt, wie die Nummerierung in einer Liste durch Kopieren einer Liste neu gestartet wird.

```csharp
Document doc = new Document();

// Eine Liste ermöglicht es uns, Absätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
 // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
 // Wir können eine Liste beginnen und beenden, indem wir die „ListFormat“-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Erstellen Sie eine Liste aus einer Microsoft Word-Vorlage und passen Sie deren erste Listenebene an.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Wenden Sie unsere Liste auf einige Absätze an.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Wir können eine Kopie einer vorhandenen Liste zur Listensammlung des Dokuments hinzufügen
// um eine ähnliche Liste zu erstellen, ohne Änderungen am Original vorzunehmen.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Die zweite Liste auf neue Absätze anwenden.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

Zeigt, wie mit Listenebenen gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Eine Liste ermöglicht es uns, Absätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
 // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
 // Wir können eine Liste beginnen und beenden, indem wir die „ListFormat“-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Nachfolgend finden Sie zwei Arten von Listen, die wir mit einem Document Builder erstellen können.
// 1 – Eine nummerierte Liste:
// Nummerierte Listen erstellen eine logische Reihenfolge für ihre Absätze, indem sie jedes Element nummerieren.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Durch Setzen der Eigenschaft „ListLevelNumber“ können wir die Listenebene erhöhen
// um eine eigenständige Unterliste beim aktuellen Listenelement zu beginnen.
// Die Microsoft Word-Listenvorlage namens „NumberDefault“ verwendet Zahlen, um Listenebenen für die erste Listenebene zu erstellen.
 // Tiefere Listenebenen verwenden Buchstaben und römische Kleinbuchstaben.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 – Eine Liste mit Aufzählungszeichen:
// Diese Liste fügt vor jedem Absatz einen Einzug und ein Aufzählungszeichen („•“) ein.
// Auf tieferen Ebenen dieser Liste werden andere Symbole verwendet, z. B. „■“ und „○“.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Wir können die Listenformatierung deaktivieren, um nachfolgende Absätze nicht als Listen zu formatieren, indem wir das Flag „Liste“ deaktivieren.
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Lists](../../aspose.words.lists/)
* Montage [Aspose.Words](../../)
