---
title: ListCollection.AddCopy
linktitle: AddCopy
articleTitle: AddCopy
second_title: Aspose.Words für .NET
description: ListCollection AddCopy methode. Erstellt eine neue Liste indem die angegebene Liste kopiert und zur Listensammlung im Dokument hinzugefügt wird in C#.
type: docs
weight: 50
url: /de/net/aspose.words.lists/listcollection/addcopy/
---
## ListCollection.AddCopy method

Erstellt eine neue Liste, indem die angegebene Liste kopiert und zur Listensammlung im Dokument hinzugefügt wird.

```csharp
public List AddCopy(List srcList)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcList | List | Die Quellliste, aus der kopiert werden soll. |

### Rückgabewert

Die neu erstellte Liste.

## Bemerkungen

Die Quellenliste kann aus einem beliebigen Dokument stammen. Wenn die Quellliste zu einem anderen Dokument gehört, wird eine Kopie der Liste erstellt und dem aktuellen Dokument hinzugefügt.

Wenn es sich bei der Quellliste um einen Verweis auf oder eine Definition eines Listenstils handelt, hat die neu erstellte Liste keinen Bezug zum ursprünglichen Listenstil.

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

// Eine Liste ermöglicht es uns, Absätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
 // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
 // Wir können eine Liste beginnen und beenden, indem wir die „ListFormat“-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Erstellen Sie eine Liste aus einer Microsoft Word-Vorlage und passen Sie deren erste Listenebene an.
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

// Wir können eine Kopie einer vorhandenen Liste zur Listensammlung des Dokuments hinzufügen
// um eine ähnliche Liste zu erstellen, ohne Änderungen am Original vorzunehmen.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Die zweite Liste auf neue Absätze anwenden.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

### Siehe auch

* class [List](../../list/)
* class [ListCollection](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
