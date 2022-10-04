---
title: NumberFormat
second_title: Aspose.Words für .NET-API-Referenz
description: Gibt das Zahlenformat für die Listenebene zurück oder legt es fest.
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

Beispielsweise erzeugt die Zeichenfolge "\x0000.\x0001)" eine Liste label , die in etwa so aussieht wie "1.5)". Die Zahl „1“ ist die aktuelle Zahl aus der 1. Listenebene, die Zahl „5“ ist die aktuelle Zahl aus der 2. Listenebene.

Null ist nicht zulässig, aber eine leere Zeichenfolge, die bedeutet, dass keine Zahl gültig ist.

### Beispiele

Zeigt, wie Sie benutzerdefinierte Listenformatierungen auf Absätze anwenden, wenn Sie DocumentBuilder verwenden.

```csharp
Document doc = new Document();

// Eine Liste ermöglicht es uns, Sätze von Absätzen mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen. 
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Dokumentenerstellers verwenden. 
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

Zeigt fortgeschrittene Möglichkeiten zum Anpassen von Listenbezeichnungen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Liste ermöglicht es uns, Sätze von Absätzen mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen. 
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Dokumentenerstellers verwenden. 
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Beschriftungen der Ebene 1 werden gemäß dem Absatzstil "Überschrift 1" formatiert und haben ein Präfix.
// Diese sehen aus wie "Anhang A", "Anhang B"...
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// Labels der Ebene 2 zeigen die aktuellen Nummern der ersten und zweiten Listenebene und haben führende Nullen.
// Wenn die erste Listenebene 1 ist, dann sehen die Listenbezeichnungen von diesen wie "Abschnitt (1.01)", "Abschnitt (1.02)"...
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// Beachten Sie, dass die übergeordnete Ebene die Nummerierung in Großbuchstaben verwendet.
// Wir können die Eigenschaft "IsLegal" so einstellen, dass arabische Zahlen für die höheren Listenebenen verwendet werden.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// Labels der Ebene 3 sind römische Ziffern in Großbuchstaben mit einem Präfix und einem Suffix und werden bei jedem Listenelement der Ebene 1 neu gestartet.
// Diese Listenlabels sehen aus wie "-I-", "-II-"...
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// Beschriftungen aller Listenebenen fett darstellen.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// Listenformatierung auf den aktuellen Absatz anwenden.
builder.ListFormat.List = list;

// Erstellen Sie Listenelemente, die alle drei unserer Listenebenen anzeigen.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
