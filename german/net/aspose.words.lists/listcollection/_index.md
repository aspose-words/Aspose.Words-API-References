---
title: ListCollection Class
linktitle: ListCollection
articleTitle: ListCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Lists.ListCollection für die effiziente Verwaltung von Aufzählungs- und nummerierten Listen und zur Verbesserung der Dokumentformatierung und -organisation.
type: docs
weight: 3920
url: /de/net/aspose.words.lists/listcollection/
---
## ListCollection class

Speichert und verwaltet die Formatierung der in einem Dokument verwendeten Aufzählungs- und Nummerierungslisten.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Listen](https://docs.aspose.com/words/net/working-with-lists/) Dokumentationsartikel.

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
| [Add](../../aspose.words.lists/listcollection/add/#add)(*[ListTemplate](../listtemplate/)*) | Erstellt eine neue Liste basierend auf einer vordefinierten Vorlage und fügt sie der Listensammlung im Dokument hinzu. |
| [Add](../../aspose.words.lists/listcollection/add/#add_1)(*[Style](../../aspose.words/style/)*) | Erstellt eine neue Liste, die auf einen Listenstil verweist, und fügt sie der Listensammlung im Dokument hinzu. |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy/)(*[List](../list/)*) | Erstellt eine neue Liste, indem die angegebene Liste kopiert und der Listensammlung im Dokument hinzugefügt wird. |
| [AddSingleLevelList](../../aspose.words.lists/listcollection/addsinglelevellist/)(*[ListTemplate](../listtemplate/)*) | Erstellt eine neue einstufige Liste basierend auf der vordefinierten Vorlage und fügt sie der Listensammlung im Dokument hinzu. |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator/)() | Ruft das Enumeratorobjekt ab, das die Listen im Dokument aufzählt. |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid/)(*int*) | Ruft eine Liste anhand einer Listenkennung ab. |

## Bemerkungen

Eine Liste in einem Microsoft Word-Dokument ist eine Reihe von Listenformatierungseigenschaften. Die Formatierung der Listen wird im`ListCollection` Sammlung getrennt von den Textabsätzen.

Sie erstellen keine Objekte dieser Klasse. Es gibt immer nur ein`ListCollection` -Objekt pro Dokument und ist über das[`Lists`](../../aspose.words/documentbase/lists/) Eigentum.

Um eine neue Liste basierend auf einer vordefinierten Listenvorlage oder basierend auf einem Listenstil zu erstellen, verwenden Sie die[`Add`](./add/) Verfahren.

Um eine neue Liste mit der gleichen Formatierung wie eine vorhandene Liste zu erstellen, verwenden Sie die[`AddCopy`](./addcopy/) Verfahren.

Um einen Absatz mit Aufzählungszeichen oder Nummerierungen zu versehen, müssen Sie die Listenformatierung auf einen Absatz anwenden, indem Sie ihm eine[`List`](../list/)Objekt zu the [`List`](../listformat/list/) Eigentum von[`ListFormat`](../listformat/).

Um die Listenformatierung aus einem Absatz zu entfernen, verwenden Sie die[`RemoveNumbers`](../listformat/removenumbers/) -Methode.

Wenn Sie sich mit WordprocessingML auskennen, wissen Sie vielleicht, dass es separate Konzepte für „Liste“ und „Listendefinition“ definiert. Dies entspricht genau der Art und Weise, wie die Listenformatierung in einem Microsoft Word-Dokument auf niedriger Ebene gespeichert wird. Die Listendefinition ist wie ein „Schema“ und die Liste wie eine Instanz einer Listendefinition.

Um das Programmiermodell zu vereinfachen, verbirgt Aspose.Words den Unterschied zwischen Liste und Listendefinition auf ähnliche Weise, wie Microsoft Word dies in seiner Benutzeroberfläche verbirgt. Dadurch können Sie sich mehr darauf konzentrieren, wie Ihr Dokument aussehen soll, anstatt Low-Level-Objekte zu erstellen, um die Anforderungen des Microsoft Word-Dateiformats zu erfüllen.

In der aktuellen Version von Aspose.Words. ist es nicht möglich, Listen zu löschen, sobald sie erstellt wurden. Dies ähnelt Microsoft Word, wo der Benutzer keine explizite Kontrolle über Listendefinitionen hat.

## Beispiele

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

* class [List](../list/)
* namensraum [Aspose.Words.Lists](../../aspose.words.lists/)
* Montage [Aspose.Words](../../)
