---
title: StyleCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words für .NET
description: StyleCollection Add methode. Erstellt einen neuen benutzerdefinierten Stil und fügt ihn der Sammlung hinzu in C#.
type: docs
weight: 60
url: /de/net/aspose.words/stylecollection/add/
---
## StyleCollection.Add method

Erstellt einen neuen benutzerdefinierten Stil und fügt ihn der Sammlung hinzu.

```csharp
public Style Add(StyleType type, string name)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| type | StyleType | A[`StyleType`](../../styletype/) Wert, der den Typ des zu erstellenden Stils angibt. |
| name | String | Groß- und Kleinschreibung beachtender Name des zu erstellenden Stils. |

## Bemerkungen

Sie können Zeichen-, Absatz- oder Listenformate erstellen.

Beim Erstellen eines Listenstils wird der Stil mit der standardmäßigen nummerierten Listenformatierung (1 \ a \ i) erstellt.

Löst eine Ausnahme aus, wenn bereits ein Stil mit diesem Namen vorhanden ist.

## Beispiele

Zeigt, wie man der Stilsammlung eines Dokuments einen Stil hinzufügt.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Standardparameter für neue Stile festlegen, die wir später möglicherweise zu dieser Sammlung hinzufügen.
styles.DefaultFont.Name = "Courier New";
// Wenn wir einen Stil von „StyleType.Paragraph“ hinzufügen, wendet die Sammlung die Werte von an
// seine „DefaultParagraphFormat“-Eigenschaft zur „ParagraphFormat“-Eigenschaft des Stils.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Fügen Sie einen Stil hinzu und überprüfen Sie dann, ob er die Standardeinstellungen hat.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

Zeigt, wie ein Listenstil erstellt und in einem Dokument verwendet wird.

```csharp
Document doc = new Document();

// Eine Liste ermöglicht es uns, Absätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
 // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
 // Wir können eine Liste beginnen und beenden, indem wir die „ListFormat“-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Wir können ein ganzes List-Objekt in einem Stil enthalten.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Ändere das Erscheinungsbild aller Listenebenen in unserer Liste.
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

// Einige Listenelemente hinzufügen, die unsere Liste formatieren wird.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Erstellen Sie eine weitere Liste basierend auf dem Listenstil und wenden Sie sie an.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### Siehe auch

* class [Style](../../style/)
* enum [StyleType](../../styletype/)
* class [StyleCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
