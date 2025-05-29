---
title: ListLevel Class
linktitle: ListLevel
articleTitle: ListLevel
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Lists.ListLevel für erweiterte Listenformatierung. Verbessern Sie die Struktur Ihres Dokuments mit leistungsstarken, anpassbaren Optionen.
type: docs
weight: 3950
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
| [Alignment](../../aspose.words.lists/listlevel/alignment/) { get; set; } | Ruft die Ausrichtung der tatsächlichen Nummer des Listenelements ab oder legt diese fest. |
| [CustomNumberStyleFormat](../../aspose.words.lists/listlevel/customnumberstyleformat/) { get; set; } | Ruft das benutzerdefinierte Zahlenformat für diese Listenebene ab oder legt es fest. Beispiel: "a, ç, ĝ, ...". |
| [Font](../../aspose.words.lists/listlevel/font/) { get; } | Gibt die für die Listenbezeichnung verwendete Zeichenformatierung an. |
| [ImageData](../../aspose.words.lists/listlevel/imagedata/) { get; } | Gibt Bilddaten der Bildaufzählungsform für die aktuelle Listenebene zurück. |
| [IsLegal](../../aspose.words.lists/listlevel/islegal/) { get; set; } | Wahr, wenn die Ebene alle übernommenen Zahlen in arabische Zahlen umwandelt, falsch, wenn ihr Zahlenstil beibehalten wird. |
| [LinkedStyle](../../aspose.words.lists/listlevel/linkedstyle/) { get; set; } | Ruft den Absatzstil ab oder legt ihn fest, der mit dieser Listenebene verknüpft ist. |
| [NumberFormat](../../aspose.words.lists/listlevel/numberformat/) { get; set; } | Gibt das Zahlenformat für die Listenebene zurück oder legt es fest. |
| [NumberPosition](../../aspose.words.lists/listlevel/numberposition/) { get; set; } | Gibt die Position (in Punkten) der Nummer oder des Aufzählungszeichens für die Listenebene zurück oder legt sie fest. |
| [NumberStyle](../../aspose.words.lists/listlevel/numberstyle/) { get; set; } | Gibt den Nummernstil für diese Listenebene zurück oder legt ihn fest. |
| [RestartAfterLevel](../../aspose.words.lists/listlevel/restartafterlevel/) { get; set; } | Legt die Listenebene fest oder gibt sie zurück, die angezeigt werden muss, bevor die Nummerierung auf der angegebenen Listenebene neu gestartet wird. |
| [StartAt](../../aspose.words.lists/listlevel/startat/) { get; set; } | Gibt die Startnummer für diese Listenebene zurück oder legt sie fest. |
| [TabPosition](../../aspose.words.lists/listlevel/tabposition/) { get; set; } | Gibt die Tabulatorposition (in Punkten) für die Listenebene zurück oder legt sie fest. |
| [TextPosition](../../aspose.words.lists/listlevel/textposition/) { get; set; } | Gibt die Position (in Punkten) für die zweite Zeile des umbrechenden Textes für die Listenebene zurück oder legt sie fest. |
| [TrailingCharacter](../../aspose.words.lists/listlevel/trailingcharacter/) { get; set; } | Gibt das nach der Zahl eingefügte Zeichen für die Listenebene zurück oder legt es fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [CreatePictureBullet](../../aspose.words.lists/listlevel/createpicturebullet/)() | Erstellt eine Bildaufzählungsform für die aktuelle Listenebene. |
| [DeletePictureBullet](../../aspose.words.lists/listlevel/deletepicturebullet/)() | Löscht das Bildaufzählungszeichen für die aktuelle Listenebene. |
| [Equals](../../aspose.words.lists/listlevel/equals/#equals)(*ListLevel*) | Vergleicht mit dem angegebenen ListLevel. |
| override [GetHashCode](../../aspose.words.lists/listlevel/gethashcode/)() | Berechnet den Hashcode für dieses Objekt. |
| static [GetEffectiveValue](../../aspose.words.lists/listlevel/geteffectivevalue/)(*int, [NumberStyle](../../aspose.words/numberstyle/), string*) | Gibt die String-Darstellung des`ListLevel`Objekt für den angegebenen Index des Listenelements. Parameter geben die[`NumberStyle`](../../aspose.words/numberstyle/) und ein optionaler Formatstring , der verwendet wird, wennCustom ist angegeben. |

## Bemerkungen

Sie erstellen keine Objekte dieser Klasse. Objekte auf Listenebene werden automatisch beim Erstellen einer Liste erstellt. Sie greifen auf`ListLevel` Objekte über the [`ListLevelCollection`](../listlevelcollection/) Sammlung.

Nutzen Sie die Eigenschaften von`ListLevel` um die Listenformatierung für einzelne Listenebenen festzulegen.

## Beispiele

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

### Siehe auch

* namensraum [Aspose.Words.Lists](../../aspose.words.lists/)
* Montage [Aspose.Words](../../)
