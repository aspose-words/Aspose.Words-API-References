---
title: ListFormat
second_title: Aspose.Words für .NET-API-Referenz
description: Ermöglicht die Steuerung welche Listenformatierung auf einen Absatz angewendet wird.
type: docs
weight: 3280
url: /de/net/aspose.words.lists/listformat/
---
## ListFormat class

Ermöglicht die Steuerung, welche Listenformatierung auf einen Absatz angewendet wird.

```csharp
public class ListFormat
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | Wahr, wenn auf den Absatz Aufzählungszeichen oder Nummerierungen angewendet wurden. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | Ruft die Liste ab oder legt sie fest, zu der dieser Absatz gehört. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | Gibt die Formatierung auf Listenebene plus alle auf den aktuellen Absatz angewendeten Formatierungsüberschreibungen zurück. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | Ruft die Nummer der Listenebene (0 bis 8) für den Absatz ab oder legt sie fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | Beginnt eine neue Standardliste mit Aufzählungszeichen und wendet sie auf den Absatz an. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | Beginnt eine neue standardmäßig nummerierte Liste und wendet sie auf den Absatz an. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | Erhöht die Listenebene des aktuellen Absatzes um eine Ebene. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | Verringert die Listenebene des aktuellen Absatzes um eine Ebene. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | Entfernt Nummern oder Aufzählungszeichen aus dem aktuellen Absatz und setzt die Listenebene auf Null. |

### Bemerkungen

Ein Absatz in einem Microsoft Word-Dokument kann mit Aufzählungszeichen oder Nummerierungen versehen werden. Wenn ein Absatz mit Aufzählungszeichen oder Nummerierungen versehen ist, wird die Listenformatierung auf den Absatz angewendet.

Sie erstellen keine Objekte der[`ListFormat`](./listformat/) Klasse direkt. Du greifst zu[`ListFormat`](./listformat/) als Eigenschaft eines anderen Objekts, dem eine Listenformatierung zugeordnet werden kann. Im Moment sind die Objekte, die eine Listenformatierung haben können:[`Paragraph`](../../aspose.words/paragraph/) , [`Style`](../../aspose.words/style/) und[`DocumentBuilder`](../../aspose.words/documentbuilder/).

[`ListFormat`](./listformat/) von a[`Paragraph`](../../aspose.words/paragraph/) gibt an, welche Listenformatierung und Listenebene auf diesen bestimmten Absatz angewendet wird.

[`ListFormat`](./listformat/) von a[`Style`](../../aspose.words/style/)(gilt nur für Absatzstile) ermöglicht die Angabe, welche Listenformatierung und Listenebene auf alle Absätze dieses bestimmten Stils angewendet wird.

[`ListFormat`](./listformat/) von a[`DocumentBuilder`](../../aspose.words/documentbuilder/) bietet Zugriff auf die Listenformatierung an der aktuellen Cursorposition innerhalb der[`DocumentBuilder`](../../aspose.words/documentbuilder/).

Die Listenformatierung selbst wird in a gespeichert[`List`](../list/) Objekt, das getrennt von den Absätzen gespeichert wird. Die Listenobjekte werden in a gespeichert[`ListCollection`](../listcollection/) Sammlung. Es gibt einen einzigen [`ListCollection`](../listcollection/) Abholung pro[`Document`](../../aspose.words/document/).

Die Absätze gehören physikalisch nicht zu einer Liste. Die Absätze just verweisen über die auf ein bestimmtes Listenobjekt[`List`](./list/) property und eine bestimmte Ebene in der Liste über die[`ListLevelNumber`](./listlevelnumber/) property. Durch Festlegen dieser beiden Eigenschaften steuern Sie, welche Aufzählungszeichen und Nummerierungen auf einen Absatz angewendet werden.

### Beispiele

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

* namensraum [Aspose.Words.Lists](../../aspose.words.lists/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
