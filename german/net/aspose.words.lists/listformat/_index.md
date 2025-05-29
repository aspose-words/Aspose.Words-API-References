---
title: ListFormat Class
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words für .NET
description: Meistern Sie die Listenformatierung in Ihren Dokumenten mit der Klasse Aspose.Words.Lists.ListFormat. Optimieren Sie mühelos den Absatzstil für bessere Lesbarkeit.
type: docs
weight: 3930
url: /de/net/aspose.words.lists/listformat/
---
## ListFormat class

Ermöglicht die Steuerung, welche Listenformatierung auf einen Absatz angewendet wird.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Listen](https://docs.aspose.com/words/net/working-with-lists/) Dokumentationsartikel.

```csharp
public class ListFormat
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | Wahr, wenn auf den Absatz Aufzählungszeichen oder Nummerierungen angewendet wurden. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | Ruft die Liste ab oder legt sie fest, zu der dieser Absatz gehört. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | Gibt die Formatierung auf Listenebene sowie alle auf den aktuellen Absatz angewendeten Formatierungsüberschreibungen zurück. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | Ruft die Listenebenennummer (0 bis 8) für den Absatz ab oder legt sie fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | Startet eine neue Standardaufzählungsliste und wendet sie auf den Absatz an. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | Startet eine neue standardmäßige nummerierte Liste und wendet sie auf den Absatz an. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | Erhöht die Listenebene des aktuellen Absatzes um eine Ebene. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | Verringert die Listenebene des aktuellen Absatzes um eine Ebene. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | Entfernt Nummerierungen oder Aufzählungszeichen aus dem aktuellen Absatz und setzt die Listenebene auf Null. |

## Bemerkungen

Ein Absatz in einem Microsoft Word-Dokument kann mit Aufzählungszeichen oder Nummerierungen versehen sein. Wenn ein Absatz mit Aufzählungszeichen oder Nummerierungen versehen ist, wird auf den Absatz die Listenformatierung angewendet.

Sie erstellen keine Objekte des`ListFormat` Klasse direkt. Sie greifen`ListFormat`als Eigenschaft eines anderen Objekts, dem eine Listenformatierung zugeordnet werden kann. Derzeit sind dies die Objekte, die eine Listenformatierung haben können:[`Paragraph`](../../aspose.words/paragraph/) , [`Style`](../../aspose.words/style/) Und[`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat` eines[`Paragraph`](../../aspose.words/paragraph/) gibt an , welche Listenformatierung und Listenebene auf diesen bestimmten Absatz angewendet wird.

`ListFormat` eines[`Style`](../../aspose.words/style/) (gilt nur für Absatzformate ) ermöglicht die Angabe, welche Listenformatierung und Listenebene auf alle Absätze dieses bestimmten Formats angewendet wird.

`ListFormat` eines[`DocumentBuilder`](../../aspose.words/documentbuilder/) ermöglicht den Zugriff auf die Listenformatierung an der aktuellen Cursorposition innerhalb der[`DocumentBuilder`](../../aspose.words/documentbuilder/).

Die Listenformatierung selbst wird in einem[`List`](../list/) Objekt, das getrennt von den Absätzen gespeichert wird. Die Listenobjekte werden in einem[`ListCollection`](../listcollection/) Sammlung. Es gibt eine einzelne [`ListCollection`](../listcollection/) Sammlung pro[`Document`](../../aspose.words/document/).

Die Absätze gehören physisch nicht zu einer Liste. Die Absätze verweisen lediglich auf ein bestimmtes Listenobjekt über die[`List`](./list/) property und einer bestimmten Ebene in der Liste über die[`ListLevelNumber`](./listlevelnumber/) property. Durch Festlegen dieser beiden Eigenschaften steuern Sie, welche Aufzählungszeichen und Nummerierungen auf einen Absatz angewendet werden.

## Beispiele

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
