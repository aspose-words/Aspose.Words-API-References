---
title: StyleCollection.GetEnumerator
second_title: Aspose.Words für .NET-API-Referenz
description: StyleCollection methode. Ruft ein Enumeratorobjekt ab das Stile in der alphabetischen Reihenfolge ihrer Namen auflistet.
type: docs
weight: 90
url: /de/net/aspose.words/stylecollection/getenumerator/
---
## StyleCollection.GetEnumerator method

Ruft ein Enumeratorobjekt ab, das Stile in der alphabetischen Reihenfolge ihrer Namen auflistet.

```csharp
public IEnumerator<Style> GetEnumerator()
```

### Beispiele

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

### Siehe auch

* class [Style](../../style/)
* class [StyleCollection](../)
* namensraum [Aspose.Words](../../stylecollection/)
* Montage [Aspose.Words](../../../)


