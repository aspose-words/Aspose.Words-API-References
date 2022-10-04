---
title: ListCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Speichert und verwaltet die Formatierung von Aufzählungs und Nummerierungslisten die in einem Dokument verwendet werden.
type: docs
weight: 3270
url: /de/net/aspose.words.lists/listcollection/
---
## ListCollection class

Speichert und verwaltet die Formatierung von Aufzählungs- und Nummerierungslisten, die in einem Dokument verwendet werden.

```csharp
public class ListCollection : IEnumerable<List>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.lists/listcollection/count/) { get; } | Ruft die Anzahl der nummerierten und Aufzählungslisten im Dokument ab. |
| [Document](../../aspose.words.lists/listcollection/document/) { get; } | Ruft das Besitzerdokument ab. |
| [Item](../../aspose.words.lists/listcollection/item/) { get; } | Ruft eine Liste nach Index ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.lists/listcollection/add/#add)(ListTemplate) | Erstellt eine neue Liste basierend auf einer vordefinierten Vorlage und fügt sie der Sammlung von Listen im Dokument hinzu. |
| [Add](../../aspose.words.lists/listcollection/add/#add_1)(Style) | Erstellt eine neue Liste, die auf einen Listenstil verweist, und fügt sie der Sammlung von Listen im Dokument hinzu. |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy/)(List) | Erstellt eine neue Liste, indem die angegebene Liste kopiert und zur Sammlung von Listen im Dokument hinzugefügt wird. |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator/)() | Ruft das Aufzählungsobjekt ab, das Listen im Dokument aufzählt. |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid/)(int) | Ruft eine Liste anhand einer Listenkennung ab. |

### Bemerkungen

Eine Liste in einem Microsoft Word-Dokument ist ein Satz von Listenformatierungseigenschaften. Die Formatierung der Listen wird in gespeichert[`ListCollection`](./listcollection/) Sammlung getrennt von den Textabsätzen.

Sie erstellen keine Objekte dieser Klasse. Es gibt immer nur einen[`ListCollection`](./listcollection/) Objekt pro Dokument und es ist über die zugänglich[`Lists`](../../aspose.words/documentbase/lists/) Eigentum.

Um eine neue Liste basierend auf einer vordefinierten Listenvorlage oder basierend auf einem Listenstil zu erstellen, verwenden Sie die[`Add`](./add/) Methode.

Um eine neue Liste mit identischer Formatierung wie eine vorhandene Liste zu erstellen, verwenden Sie [`AddCopy`](./addcopy/) Methode.

Um einen Absatz mit Aufzählungszeichen oder Nummern zu versehen, müssen Sie list formatting auf einen Absatz anwenden, indem Sie a zuweisen[`List`](../list/) Einspruch gegen the [`List`](../listformat/list/) Eigentum von[`ListFormat`](../listformat/).

Um die Listenformatierung aus einem Absatz zu entfernen, verwenden Sie die[`RemoveNumbers`](../listformat/removenumbers/) Methode.

Wenn Sie etwas über WordprocessingML wissen, wissen Sie vielleicht, dass es separate Konzepte für "Liste" und "Listendefinition" definiert. Dies entspricht genau der Art und Weise, wie Listenformatierungen in einem Microsoft Word-Dokument auf niedriger Ebene gespeichert werden. Die Listendefinition ist wie ein "Schema" und list ist wie eine Instanz einer Listendefinition.

Um das Programmiermodell zu vereinfachen, verbirgt Aspose.Words die Unterscheidung zwischen list und list -Definition ähnlich wie Microsoft Word dies in seiner Benutzeroberfläche verbirgt. Dadurch können Sie sich mehr darauf konzentrieren, wie Ihr Dokument aussehen soll, anstatt Erstellen von Low-Level-Objekten, um die Anforderungen des Microsoft Word-Dateiformats zu erfüllen.

Es ist nicht möglich, Listen zu löschen, sobald sie in der aktuellen Version von Aspose.Words. erstellt wurden. Dies ähnelt Microsoft Word, wo der Benutzer keine explizite Kontrolle über Listendefinitionen hat.

### Beispiele

Zeigt, wie ein Dokument mit einem Beispiel aller Listen aus einem anderen Dokument erstellt wird.

```csharp
public void PrintOutAllLists()
{
    Document srcDoc = new Document(MyDir + "Rendering.docx");

    Document dstDoc = new Document();
    DocumentBuilder builder = new DocumentBuilder(dstDoc);

    foreach (List srcList in srcDoc.Lists)
    {
        List dstList = dstDoc.Lists.AddCopy(srcList);
        AddListSample(builder, dstList);
    }

    dstDoc.Save(ArtifactsDir + "Lists.PrintOutAllLists.docx");
}

private static void AddListSample(DocumentBuilder builder, List list)
{
    builder.Writeln("Sample formatting of list with ListId:" + list.ListId);
    builder.ListFormat.List = list;
    for (int i = 0; i < list.ListLevels.Count; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }

    builder.ListFormat.RemoveNumbers();
    builder.Writeln();
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

* class [List](../list/)
* namensraum [Aspose.Words.Lists](../../aspose.words.lists/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
