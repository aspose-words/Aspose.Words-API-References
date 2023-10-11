---
title: Class ListFormat
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Lists.ListFormat klas. Ermöglicht die Steuerung welche Listenformatierung auf einen Absatz angewendet wird.
type: docs
weight: 3480
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
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | True, wenn auf den Absatz eine Aufzählungs- oder Nummernformatierung angewendet wurde. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | Ruft die Liste ab, zu der dieser Absatz gehört, oder legt sie fest. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | Gibt die Formatierung auf Listenebene plus alle auf den aktuellen Absatz angewendeten Formatierungsüberschreibungen zurück. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | Ruft die Listenebenennummer (0 bis 8) für den Absatz ab oder legt diese fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | Startet eine neue Standardliste mit Aufzählungszeichen und wendet sie auf den Absatz an. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | Startet eine neue standardmäßige nummerierte Liste und wendet sie auf den Absatz an. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | Erhöht die Listenebene des aktuellen Absatzes um eine Ebene. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | Verringert die Listenebene des aktuellen Absatzes um eine Ebene. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | Entfernt Zahlen oder Aufzählungszeichen aus dem aktuellen Absatz und setzt die Listenebene auf Null. |

### Bemerkungen

Ein Absatz in einem Microsoft Word-Dokument kann mit Aufzählungszeichen oder Nummerierung versehen sein. Wenn ein Absatz mit Aufzählungszeichen oder Nummerierung versehen ist, spricht man von einer Listenformatierung , die auf den Absatz angewendet wird.

Sie erstellen keine Objekte der`ListFormat` Klasse direkt. Sie greifen zu`ListFormat` als Eigenschaft eines anderen Objekts, dem eine Listenformatierung zugeordnet werden kann. Im Moment sind die Objekte, die eine Listenformatierung haben können:[`Paragraph`](../../aspose.words/paragraph/) , [`Style`](../../aspose.words/style/) Und[`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat` von einem[`Paragraph`](../../aspose.words/paragraph/) Gibt an, welche Listenformatierung und Listenebene auf diesen bestimmten Absatz angewendet wird.

`ListFormat` von einem[`Style`](../../aspose.words/style/) (anwendbar nur auf Absatzstile) ermöglicht die Angabe, welche Listenformatierung und Listenebene auf alle Absätze dieses bestimmten Stils angewendet wird.

`ListFormat` von einem[`DocumentBuilder`](../../aspose.words/documentbuilder/) bietet Zugriff auf die Listenformatierung an der aktuellen Cursorposition innerhalb der[`DocumentBuilder`](../../aspose.words/documentbuilder/).

Die Listenformatierung selbst wird in a gespeichert[`List`](../list/) -Objekt, das getrennt von den Absätzen gespeichert wird. Die Listenobjekte werden in a gespeichert[`ListCollection`](../listcollection/) Sammlung. Es gibt ein einzelnes [`ListCollection`](../listcollection/) Sammlung pro[`Document`](../../aspose.words/document/).

Die Absätze gehören physisch nicht zu einer Liste. Die Absätze just verweisen über das auf ein bestimmtes Listenobjekt[`List`](./list/) property und eine bestimmte Ebene in der Liste über die[`ListLevelNumber`](./listlevelnumber/) property. Durch Festlegen dieser beiden Eigenschaften steuern Sie, welche Aufzählungszeichen und Nummerierungen auf einen Absatz angewendet werden.

### Beispiele

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


