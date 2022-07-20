---
title: Add
second_title: Aspose.Words für .NET-API-Referenz
description: Erstellt eine neue Liste basierend auf einer vordefinierten Vorlage und fügt sie der Sammlung von Listen im Dokument hinzu.
type: docs
weight: 40
url: /de/net/aspose.words.lists/listcollection/add/
---
## Add(ListTemplate) {#add}

Erstellt eine neue Liste basierend auf einer vordefinierten Vorlage und fügt sie der Sammlung von Listen im Dokument hinzu.

```csharp
public List Add(ListTemplate listTemplate)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| listTemplate | ListTemplate | Die Vorlage der Liste. |

### Rückgabewert

Die neu erstellte Liste.

### Bemerkungen

Aspose.Words-Listenvorlagen entsprechen den 21 Listenvorlagen available im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word 2003.

Alle mit dieser Methode erstellten Listen haben 9 Listenebenen.

### Beispiele

Zeigt, wie Sie eine Liste erstellen, indem Sie ein neues Listenformat auf eine Sammlung von Absätzen anwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1");
builder.Writeln("Paragraph 2");
builder.Write("Paragraph 3");

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

Assert.AreEqual(0, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));

List list = doc.Lists.Add(ListTemplate.NumberUppercaseLetterDot);

foreach (Paragraph paragraph in paras.OfType<Paragraph>())
{
    paragraph.ListFormat.List = list;
    paragraph.ListFormat.ListLevelNumber = 1;
}

Assert.AreEqual(3, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));
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

* class [List](../../list)
* enum [ListTemplate](../../listtemplate)
* class [ListCollection](../../listcollection)
* namensraum [Aspose.Words.Lists](../../listcollection)
* Montage [Aspose.Words](../../../)

---

## Add(Style) {#add_1}

Erstellt eine neue Liste, die auf einen Listenstil verweist, und fügt sie der Sammlung von Listen im Dokument hinzu.

```csharp
public List Add(Style listStyle)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| listStyle | Style | Der Listenstil. |

### Rückgabewert

Die neu erstellte Liste.

### Bemerkungen

Die neu erstellte Liste referenziert den Listenstil. Wenn Sie die Eigenschaften des Stils list ändern, wird dies in den Eigenschaften der Liste widergespiegelt. Wenn Sie umgekehrt die properties der Liste ändern, spiegelt sich dies in den Eigenschaften des Listenstils wider.

### Beispiele

Zeigt, wie ein Listenstil erstellt und in einem Dokument verwendet wird.

```csharp
Document doc = new Document();

// Eine Liste ermöglicht es uns, Sätze von Absätzen mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen. 
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Dokumentenerstellers verwenden. 
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Wir können ein ganzes List-Objekt in einem Stil enthalten.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Ändern Sie das Aussehen aller Listenebenen in unserer Liste.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// Eine weitere Liste aus einer Liste innerhalb eines Stils erstellen.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// Fügen Sie einige Listenelemente hinzu, die unsere Liste formatieren wird.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Eine weitere Liste basierend auf dem Listenstil erstellen und anwenden.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### Siehe auch

* class [List](../../list)
* class [Style](../../../aspose.words/style)
* class [ListCollection](../../listcollection)
* namensraum [Aspose.Words.Lists](../../listcollection)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
