---
title: ListLevel Class
linktitle: ListLevel
articleTitle: ListLevel
second_title: Aspose.Words für .NET
description: Aspose.Words.Lists.ListLevel klas. Definiert die Formatierung für eine Listenebene in C#.
type: docs
weight: 3500
url: /de/net/aspose.words.lists/listlevel/
---
## ListLevel class

Definiert die Formatierung für eine Listenebene.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Listen](https://docs.aspose.com/words/net/working-with-lists/) Dokumentationsartikel.

```csharp
public class ListLevel
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Alignment](../../aspose.words.lists/listlevel/alignment/) { get; set; } | Ruft die Begründung der tatsächlichen Nummer des Listenelements ab oder legt diese fest. |
| [CustomNumberStyleFormat](../../aspose.words.lists/listlevel/customnumberstyleformat/) { get; } | Ruft das benutzerdefinierte Zahlenstilformat für diese Listenebene ab. Zum Beispiel: „a, ç, ĝ, ...“. |
| [Font](../../aspose.words.lists/listlevel/font/) { get; } | Gibt die Zeichenformatierung an, die für die Listenbezeichnung verwendet wird. |
| [ImageData](../../aspose.words.lists/listlevel/imagedata/) { get; } | Gibt Bilddaten der Bildaufzählungsform für die aktuelle Listenebene zurück. |
| [IsLegal](../../aspose.words.lists/listlevel/islegal/) { get; set; } | True, wenn die Ebene alle geerbten Zahlen in Arabisch umwandelt, false, wenn ihr Zahlenstil erhalten bleibt. |
| [LinkedStyle](../../aspose.words.lists/listlevel/linkedstyle/) { get; set; } | Ruft den Absatzstil ab, der mit dieser Listenebene verknüpft ist, oder legt diesen fest. |
| [NumberFormat](../../aspose.words.lists/listlevel/numberformat/) { get; set; } | Gibt das Zahlenformat für die Listenebene zurück oder legt es fest. |
| [NumberPosition](../../aspose.words.lists/listlevel/numberposition/) { get; set; } | Gibt die Position (in Punkten) der Zahl oder des Aufzählungszeichens für die Listenebene zurück oder legt sie fest. |
| [NumberStyle](../../aspose.words.lists/listlevel/numberstyle/) { get; set; } | Gibt den Zahlenstil für diese Listenebene zurück oder legt ihn fest. |
| [RestartAfterLevel](../../aspose.words.lists/listlevel/restartafterlevel/) { get; set; } | Legt die Listenebene fest, die angezeigt werden muss, bevor die angegebene Listenebene die Nummerierung neu startet, oder gibt sie zurück. |
| [StartAt](../../aspose.words.lists/listlevel/startat/) { get; set; } | Gibt die Startnummer für diese Listenebene zurück oder setzt sie. |
| [TabPosition](../../aspose.words.lists/listlevel/tabposition/) { get; set; } | Gibt die Tabulatorposition (in Punkt) für die Listenebene zurück oder legt sie fest. |
| [TextPosition](../../aspose.words.lists/listlevel/textposition/) { get; set; } | Gibt die Position (in Punkt) für die zweite Zeile des Umbruchtextes für die Listenebene zurück oder legt sie fest. |
| [TrailingCharacter](../../aspose.words.lists/listlevel/trailingcharacter/) { get; set; } | Gibt das nach der Nummer für die Listenebene eingefügte Zeichen zurück oder setzt es. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [CreatePictureBullet](../../aspose.words.lists/listlevel/createpicturebullet/)() | Erstellt eine Bildaufzählungsform für die aktuelle Listenebene. |
| [DeletePictureBullet](../../aspose.words.lists/listlevel/deletepicturebullet/)() | Löscht Bildaufzählungszeichen für die aktuelle Listenebene. |
| [Equals](../../aspose.words.lists/listlevel/equals/#equals)(*ListLevel*) | Vergleicht mit dem angegebenen ListLevel. |
| override [GetHashCode](../../aspose.words.lists/listlevel/gethashcode/)() | Berechnet den Hash-Code für dieses Objekt. |
| static [GetEffectiveValue](../../aspose.words.lists/listlevel/geteffectivevalue/)(*int, [NumberStyle](../../aspose.words/numberstyle/), string*) | Meldet die Zeichenfolgendarstellung von`ListLevel`Objekt für den angegebenen index des Listenelements. Parameter geben die an[`NumberStyle`](../../aspose.words/numberstyle/) und ein optionales Format string , das verwendet wird, wennCustom angegeben ist. |

## Bemerkungen

Sie erstellen keine Objekte dieser Klasse. Objekte auf Listenebene werden automatisch erstellt, wenn eine Liste erstellt wird. Sie greifen zu`ListLevel` Objekte über the [`ListLevelCollection`](../listlevelcollection/) Sammlung.

Nutzen Sie die Eigenschaften von`ListLevel` um Listenformatierung für einzelne Listenebenen anzugeben.

## Beispiele

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

### Siehe auch

* namensraum [Aspose.Words.Lists](../../aspose.words.lists/)
* Montage [Aspose.Words](../../)
