---
title: ListLevel.StartAt
second_title: Aspose.Words für .NET-API-Referenz
description: ListLevel eigendom. Gibt die Startnummer für diese Listenebene zurück oder setzt sie.
type: docs
weight: 110
url: /de/net/aspose.words.lists/listlevel/startat/
---
## ListLevel.StartAt property

Gibt die Startnummer für diese Listenebene zurück oder setzt sie.

```csharp
public int StartAt { get; set; }
```

### Bemerkungen

Der Standardwert ist 1.

### Beispiele

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

### Siehe auch

* class [ListLevel](../)
* namensraum [Aspose.Words.Lists](../../listlevel/)
* Montage [Aspose.Words](../../../)


