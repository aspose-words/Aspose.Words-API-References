---
title: StyleCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode „StyleCollection Add“, um mühelos benutzerdefinierte Stile zu erstellen und zu Ihrer Sammlung hinzuzufügen und so Ihre Designflexibilität zu verbessern.
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
| name | String | Der Name des zu erstellenden Stils muss Groß- und Kleinschreibung beachten. |

## Bemerkungen

Sie können einen Zeichen-, Absatz- oder Listenstil erstellen.

Beim Erstellen eines Listenstils wird der Stil mit der standardmäßigen nummerierten Listenformatierung (1 \ a \ i) erstellt.

Löst eine Ausnahme aus, wenn ein Stil mit diesem Namen bereits vorhanden ist.

## Beispiele

Zeigt, wie der Stilsammlung eines Dokuments ein Stil hinzugefügt wird.

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// Legen Sie Standardparameter für neue Stile fest, die wir dieser Sammlung später hinzufügen können.
styles.DefaultFont.Name = "Courier New";
// Wenn wir einen Stil vom Typ "StyleType.Paragraph" hinzufügen, wendet die Sammlung die Werte von
// seine Eigenschaft „DefaultParagraphFormat“ zur Eigenschaft „ParagraphFormat“ des Stils.
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// Fügen Sie einen Stil hinzu und überprüfen Sie dann, ob er die Standardeinstellungen hat.
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

Zeigt, wie Sie einen Listenstil erstellen und in einem Dokument verwenden.

```csharp
Document doc = new Document();

// Eine Liste ermöglicht es uns, Absatzsätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
    // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
    // Wir können eine Liste beginnen und beenden, indem wir die Eigenschaft „ListFormat“ eines Dokument-Generators verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Wir können ein ganzes Listenobjekt in einem Stil enthalten.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Ändern Sie das Erscheinungsbild aller Listenebenen in unserer Liste.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// Erstellen Sie eine weitere Liste aus einer Liste innerhalb eines Stils.
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

// Erstellen und wenden Sie eine weitere Liste basierend auf dem Listenstil an.
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
