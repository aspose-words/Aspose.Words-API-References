---
title: ListTemplate
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt eines der vordefinierten Listenformate an die in Microsoft Word verfügbar sind.
type: docs
weight: 3330
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
| BulletDefault | `0` | Standardliste mit Aufzählungszeichen mit 9 Ebenen. Aufzählungszeichen der ersten Ebene ist eine Scheibe, Aufzählungszeichen der zweiten Ebene ist ein Kreis, Aufzählungszeichen der dritten Ebene ist ein Quadrat. Dann wiederholt sich die Formatierung für die verbleibenden Ebenen. |
| BulletDisk | `0` | Dasselbe wie BulletDefault. |
| BulletCircle | `1` | Die Kugel der ersten Ebene ist ein Kreis. Die restlichen Ebenen sind dieselben wie in BulletDefault. |
| BulletSquare | `2` | Die Kugel der ersten Ebene ist ein Quadrat. Die restlichen Ebenen sind dieselben wie in BulletDefault. |
| BulletDiamonds | `3` | Die Kugel des ersten Levels ist ein Wingding-Charakter mit 4 Diamanten. Die restlichen Ebenen sind dieselben wie in BulletDefault. |
| BulletArrowHead | `4` | Die Kugel des ersten Levels ist eine Wingding-Figur mit Pfeilspitze. Die restlichen Ebenen sind dieselben wie in BulletDefault. |
| BulletTick | `5` | Die Kugel des ersten Levels ist ein Tick Wingding-Charakter. Die restlichen Ebenen sind dieselben wie in BulletDefault. |
| NumberDefault | `6` | Nummerierte Standardliste mit 9 Ebenen. Arabische Nummerierung (1., 2., 3., ...) für die erste Ebene, Kleinbuchstabennummerierung (a., b., c., ...) für die zweite Ebene, Kleinbuchstabenrömische Nummerierung (i ., ii., iii., ...) für die dritte Ebene. Dann wird die Formatierung für die verbleibenden Ebenen wiederholt. |
| NumberArabicDot | `6` | Dasselbe wie NumberDefault. |
| NumberArabicParenthesis | `7` | Die Nummer der ersten Ebene ist "1)". Die restlichen Ebenen sind die gleichen wie in NumberDefault. |
| NumberUppercaseRomanDot | `8` | Die Nummer der ersten Ebene ist "I.". Die restlichen Ebenen sind die gleichen wie in NumberDefault. |
| NumberUppercaseLetterDot | `9` | Die Nummer der ersten Ebene ist "A.". Die restlichen Ebenen sind die gleichen wie in NumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | Die Nummer der ersten Ebene ist "a)". Die restlichen Ebenen sind die gleichen wie in NumberDefault. |
| NumberLowercaseLetterDot | `11` | Die Nummer der ersten Ebene ist "a.". Die restlichen Ebenen sind die gleichen wie in NumberDefault. |
| NumberLowercaseRomanDot | `12` | Die Nummer der ersten Ebene ist "i.". Die restlichen Ebenen sind die gleichen wie in NumberDefault. |
| OutlineNumbers | `13` | Eine Gliederungsliste mit den Nummern "1), a), i), (1), (a), (i), 1., a., i.". |
| OutlineLegal | `14` | Eine Gliederungsliste mit Ebenen ist mit "1., 1.1., 1.1.1, ..." nummeriert. |
| OutlineBullets | `15` | Eine Gliederungsliste mit verschiedenen Aufzählungszeichen für verschiedene Ebenen. |
| OutlineHeadingsArticleSection | `16` | Eine Gliederungsliste mit Ebenen, die mit Überschriftenstilen verknüpft sind. |
| OutlineHeadingsLegal | `17` | Eine Gliederungsliste mit Ebenen, die mit Überschriftenstilen verknüpft sind. |
| OutlineHeadingsNumbers | `18` | Eine Gliederungsliste mit Ebenen, die mit Überschriftenstilen verknüpft sind. |
| OutlineHeadingsChapter | `19` | Eine Gliederungsliste mit Ebenen, die mit Überschriftenstilen verknüpft sind. |

### Bemerkungen

Ein Listenvorlagenwert wird als Parameter in the verwendet.[`Add`](../listcollection/add) Methode.

Aspose.Words-Listenvorlagen entsprechen den 21 Listenvorlagen available im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word 2003.

### Beispiele

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

Zeigt, wie die Nummerierung in einer Liste neu gestartet wird, indem eine Liste kopiert wird.

```csharp
Document doc = new Document();

// Eine Liste ermöglicht es uns, Sätze von Absätzen mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen. 
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Dokumentenerstellers verwenden. 
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Erstellen Sie eine Liste aus einer Microsoft Word-Vorlage und passen Sie die erste Listenebene an.
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

// Wir können eine Kopie einer bestehenden Liste zur Listensammlung des Dokuments hinzufügen
// um eine ähnliche Liste zu erstellen, ohne Änderungen am Original vorzunehmen.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Wende die zweite Liste auf neue Absätze an.
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

// Eine Liste ermöglicht es uns, Sätze von Absätzen mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen. 
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Dokumentenerstellers verwenden. 
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Unten sind zwei Arten von Listen, die wir mit einem Document Builder erstellen können.
// 1 - Eine nummerierte Liste:
// Nummerierte Listen schaffen eine logische Reihenfolge für ihre Absätze, indem sie jedes Element nummerieren.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Durch Setzen der Eigenschaft "ListLevelNumber" können wir die Listenebene erhöhen
// um eine eigenständige Unterliste am aktuellen Listenelement zu beginnen.
// Die Microsoft Word-Listenvorlage mit dem Namen "NumberDefault" verwendet Zahlen, um Listenebenen für die erste Listenebene zu erstellen.
// Tiefere Listenebenen verwenden Buchstaben und römische Ziffern in Kleinbuchstaben. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Eine Liste mit Aufzählungszeichen:
// Diese Liste fügt vor jedem Absatz einen Einzug und ein Aufzählungszeichen ("•") ein.
// Tiefere Ebenen dieser Liste verwenden andere Symbole, wie "■" und "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Wir können die Listenformatierung deaktivieren, um nachfolgende Absätze nicht als Listen zu formatieren, indem wir das "List"-Flag deaktivieren.
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Lists](../../aspose.words.lists)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
