---
title: ListLevel.NumberFormat
second_title: Aspose.Words für .NET-API-Referenz
description: ListLevel eigendom. Gibt das Zahlenformat für die Listenebene zurück oder legt es fest.
type: docs
weight: 70
url: /de/net/aspose.words.lists/listlevel/numberformat/
---
## ListLevel.NumberFormat property

Gibt das Zahlenformat für die Listenebene zurück oder legt es fest.

```csharp
public string NumberFormat { get; set; }
```

### Bemerkungen

Neben normalen Textzeichen kann die Zeichenfolge Platzhalterzeichen \x0000 bis \x0008 enthalten, die die Zahlen aus den entsprechenden Listenebenen darstellen.

Beispielsweise generiert die Zeichenfolge „\x0000.\x0001)“ eine Liste label , die etwa wie „1.5)“ aussieht. Die Zahl „1“ ist die aktuelle Nummer aus der 1. Listenebene, die Zahl „5“ ist die aktuelle Nummer aus der 2. Listenebene.

Null ist nicht zulässig, aber eine leere Zeichenfolge, d. h. keine Zahl, ist gültig.

### Beispiele

Zeigt, wie Sie bei Verwendung von DocumentBuilder eine benutzerdefinierte Listenformatierung auf Absätze anwenden.

```csharp
Document doc = new Document();

// Eine Liste ermöglicht es uns, Absätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
 // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
 // Wir können eine Liste beginnen und beenden, indem wir die „ListFormat“-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Erstellen Sie eine Liste aus einer Microsoft Word-Vorlage und passen Sie die ersten beiden Listenebenen an.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Dieser NumberFormat-Wert erstellt sternförmige Aufzählungssymbole.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Absätze erstellen und beide Listenebenen unserer benutzerdefinierten Listenformatierung darauf anwenden.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

Zeigt erweiterte Möglichkeiten zum Anpassen von Listenbeschriftungen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Liste ermöglicht es uns, Absätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
 // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
 // Wir können eine Liste beginnen und beenden, indem wir die „ListFormat“-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Beschriftungen der Ebene 1 werden entsprechend dem Absatzstil „Überschrift 1“ formatiert und haben ein Präfix.
// Diese sehen wie „Anhang A“, „Anhang B“ aus...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// Beschriftungen der Ebene 2 zeigen die aktuellen Nummern der ersten und zweiten Listenebene an und haben führende Nullen.
// Wenn die erste Listenebene 1 ist, sehen die Listenbezeichnungen dieser Listen wie „Abschnitt (1.01)“, „Abschnitt (1.02)“ aus ...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// Beachten Sie, dass die übergeordnete Ebene die Nummerierung in Großbuchstaben verwendet.
// Wir können die Eigenschaft „IsLegal“ so einstellen, dass für die höheren Listenebenen arabische Zahlen verwendet werden.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// Beschriftungen der Ebene 3 bestehen aus großen römischen Ziffern mit einem Präfix und einem Suffix und beginnen bei jedem Element der Listenebene 1 neu.
// Diese Listenbezeichnungen sehen wie folgt aus: „-I-“, „-II-“...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// Beschriftungen aller Listenebenen fett formatieren.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// Listenformatierung auf den aktuellen Absatz anwenden.
builder.ListFormat.List = list;

// Listenelemente erstellen, die alle drei unserer Listenebenen anzeigen.
for (int n = 0; n < 2; n++)
{
    for (int i = 0; i < 3; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }
}

builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.CreateListRestartAfterHigher.docx");
```

### Siehe auch

* class [ListLevel](../)
* namensraum [Aspose.Words.Lists](../../listlevel/)
* Montage [Aspose.Words](../../../)


