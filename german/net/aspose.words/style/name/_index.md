---
title: Style.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words für .NET
description: Style Name eigendom. Ruft den Namen des Stils ab oder legt ihn fest in C#.
type: docs
weight: 120
url: /de/net/aspose.words/style/name/
---
## Style.Name property

Ruft den Namen des Stils ab oder legt ihn fest.

```csharp
public string Name { get; set; }
```

## Bemerkungen

Darf keine leere Zeichenfolge sein.

Wenn in der Sammlung bereits ein Stil mit diesem Namen vorhanden ist, wird dieser Stil überschrieben. Alle betroffenen Knoten verweisen auf den neuen Stil.

## Beispiele

Zeigt, wie auf die Stilsammlung eines Dokuments zugegriffen wird.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Alle Stile aufzählen und auflisten, die ein mit Aspose.Words erstelltes Dokument standardmäßig enthält.
using (IEnumerator<Style> stylesEnum = doc.Styles.GetEnumerator())
{
    while (stylesEnum.MoveNext())
    {
        Style curStyle = stylesEnum.Current;
        Console.WriteLine($"Style name:\t\"{curStyle.Name}\", of type \"{curStyle.Type}\"");
        Console.WriteLine($"\tSubsequent style:\t{curStyle.NextParagraphStyleName}");
        Console.WriteLine($"\tIs heading:\t\t\t{curStyle.IsHeading}");
        Console.WriteLine($"\tIs QuickStyle:\t\t{curStyle.IsQuickStyle}");

        Assert.AreEqual(doc, curStyle.Document);
    }
}
```

Zeigt, wie der Stil eines Dokuments geklont wird.

```csharp
Document doc = new Document();

// Die AddCopy-Methode erstellt eine Kopie des angegebenen Stils und
// generiert automatisch einen neuen Namen für den Stil, z. B. „Überschrift 1_0“.
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

// Verwenden Sie die Eigenschaft „Name“ des Stils, um den identifizierenden Namen des Stils zu ändern.
newStyle.Name = "My Heading 1";

// Unser Dokument hat jetzt zwei identisch aussehende Stile mit unterschiedlichen Namen.
// Das Ändern der Einstellungen eines Stils hat keinen Einfluss auf den anderen.
newStyle.Font.Color = Color.Red;

Assert.AreEqual("My Heading 1", newStyle.Name);
Assert.AreEqual("Heading 1", doc.Styles["Heading 1"].Name);

Assert.AreEqual(doc.Styles["Heading 1"].Type, newStyle.Type);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Name, newStyle.Font.Name);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Size, newStyle.Font.Size);
Assert.AreNotEqual(doc.Styles["Heading 1"].Font.Color, newStyle.Font.Color);
```

### Siehe auch

* class [Style](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
