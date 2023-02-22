---
title: Style.Document
second_title: Aspose.Words für .NET-API-Referenz
description: Style eigendom. Ruft das Besitzerdokument ab.
type: docs
weight: 40
url: /de/net/aspose.words/style/document/
---
## Style.Document property

Ruft das Besitzerdokument ab.

```csharp
public DocumentBase Document { get; }
```

### Beispiele

Zeigt, wie auf die Stilsammlung eines Dokuments zugegriffen wird.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Aufzählen und Auflisten aller Stile, die ein mit Aspose.Words erstelltes Dokument standardmäßig enthält.
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

* class [DocumentBase](../../documentbase/)
* class [Style](../)
* namensraum [Aspose.Words](../../style/)
* Montage [Aspose.Words](../../../)


