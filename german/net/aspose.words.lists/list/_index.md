---
title: List Class
linktitle: List
articleTitle: List
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.Lists.List-Klasse für leistungsstarke Listenformatierung. Optimieren Sie Ihre Dokumente durch nahtlose Organisation und professionelle Präsentation.
type: docs
weight: 3910
url: /de/net/aspose.words.lists/list/
---
## List class

Stellt die Formatierung einer Liste dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Listen](https://docs.aspose.com/words/net/working-with-lists/) Dokumentationsartikel.

```csharp
public class List : IComparable<List>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Document](../../aspose.words.lists/list/document/) { get; } | Ruft das Besitzerdokument ab. |
| [IsListStyleDefinition](../../aspose.words.lists/list/isliststyledefinition/) { get; } | Rückgaben`WAHR` wenn diese Liste eine Definition eines Listenstils ist. |
| [IsListStyleReference](../../aspose.words.lists/list/isliststylereference/) { get; } | Rückgaben`WAHR` wenn diese Liste ein Verweis auf einen Listenstil ist. |
| [IsMultiLevel](../../aspose.words.lists/list/ismultilevel/) { get; } | Rückgaben`WAHR` wenn die Liste 9 Ebenen enthält;`FALSCH` wenn 1 Ebene. |
| [IsRestartAtEachSection](../../aspose.words.lists/list/isrestartateachsection/) { get; set; } | Gibt an, ob die Liste bei jedem Abschnitt neu gestartet werden soll. Der Standardwert ist`FALSCH` . |
| [ListId](../../aspose.words.lists/list/listid/) { get; } | Ruft die eindeutige Kennung der Liste ab. |
| [ListLevels](../../aspose.words.lists/list/listlevels/) { get; } | Ruft die Auflistung der Listenebenen für diese Liste ab. |
| [Style](../../aspose.words.lists/list/style/) { get; } | Ruft den Listenstil ab, auf den diese Liste verweist oder den sie definiert. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto)(*List*) | Vergleicht die angegebene Liste mit der aktuellen Liste. |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto_1)(*object*) | Vergleicht das angegebene Objekt mit dem aktuellen Objekt. |
| [Equals](../../aspose.words.lists/list/equals/#equals)(*List*) | Vergleicht mit der angegebenen Liste. |
| override [Equals](../../aspose.words.lists/list/equals/#equals_1)(*object*) | Bestimmt, ob das angegebene Objekt den gleichen Wert wie das aktuelle Objekt hat. |
| override [GetHashCode](../../aspose.words.lists/list/gethashcode/)() | Berechnet den Hashcode für dieses Listenobjekt. |
| [HasSameTemplate](../../aspose.words.lists/list/hassametemplate/)(*List*) | Gibt „true“ zurück, wenn die aktuelle Liste und die angegebene Liste aus derselben Vorlage erstellt wurden. |

## Bemerkungen

Eine Liste in einem Microsoft Word-Dokument ist eine Reihe von Listenformatierungseigenschaften. Jede Liste kann bis zu 9 Ebenen haben und Formatierungseigenschaften wie Nummerierungsstil, Startwert, Einzug, Tabulatorposition usw. werden für jede Ebene separat definiert.

A`List` Objekt gehört immer zum[`ListCollection`](../listcollection/) Sammlung.

Um eine neue Liste zu erstellen, verwenden Sie die Add-Methoden des[`ListCollection`](../listcollection/) Sammlung.

Um die Formatierung einer Liste zu ändern, verwenden Sie[`ListLevel`](../listlevel/) Objekte gefunden in die[`ListLevels`](./listlevels/) Sammlung.

Um Listenformatierungen auf einen Absatz anzuwenden oder daraus zu entfernen, verwenden Sie[`ListFormat`](../listformat/).

## Beispiele

Zeigt, wie die Nummerierung in einer Liste durch Kopieren einer Liste neu gestartet wird.

```csharp
Document doc = new Document();

// Eine Liste ermöglicht es uns, Absatzsätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
    // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
    // Wir können eine Liste beginnen und beenden, indem wir die Eigenschaft „ListFormat“ eines Dokument-Generators verwenden.
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

// Wir können der Listensammlung des Dokuments eine Kopie einer vorhandenen Liste hinzufügen
// um eine ähnliche Liste zu erstellen, ohne Änderungen am Original vorzunehmen.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Wenden Sie die zweite Liste auf neue Absätze an.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

Zeigt, wie Sie bei Verwendung von DocumentBuilder eine benutzerdefinierte Listenformatierung auf Absätze anwenden.

```csharp
Document doc = new Document();

// Eine Liste ermöglicht es uns, Absatzsätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
    // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
    // Wir können eine Liste beginnen und beenden, indem wir die Eigenschaft „ListFormat“ eines Dokument-Generators verwenden.
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

// Dieser NumberFormat-Wert erstellt sternförmige Aufzählungslistensymbole.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Erstellen Sie Absätze und wenden Sie beide Listenebenen unserer benutzerdefinierten Listenformatierung darauf an.
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

Zeigt, wie mit Listenebenen gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Eine Liste ermöglicht es uns, Absatzsätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
    // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
    // Wir können eine Liste beginnen und beenden, indem wir die Eigenschaft „ListFormat“ eines Dokument-Generators verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Unten sind zwei Arten von Listen, die wir mit einem Dokumentgenerator erstellen können.
// 1 - Eine nummerierte Liste:
// Nummerierte Listen erstellen eine logische Reihenfolge ihrer Absätze, indem sie jedes Element nummerieren.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Durch Setzen der Eigenschaft „ListLevelNumber“ können wir die Listenebene erhöhen
// um eine in sich geschlossene Unterliste beim aktuellen Listenelement zu beginnen.
// Die Microsoft Word-Listenvorlage mit dem Namen „NumberDefault“ verwendet Zahlen, um Listenebenen für die erste Listenebene zu erstellen.
    // Tiefere Listenebenen verwenden Buchstaben und römische Ziffern in Kleinbuchstaben.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Eine Aufzählungsliste:
// Diese Liste wendet vor jedem Absatz einen Einzug und ein Aufzählungszeichen („•“) an.
// Tiefere Ebenen dieser Liste verwenden andere Symbole, wie „■“ und „○“.
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
