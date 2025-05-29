---
title: Style.Styles
linktitle: Styles
articleTitle: Styles
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Stilstile“, um auf eine kuratierte Sammlung von Stilen zuzugreifen und Ihr Design mit einer einzigartigen, zusammenhängenden Ästhetik aufzuwerten.
type: docs
weight: 190
url: /de/net/aspose.words/style/styles/
---
## Style.Styles property

Ruft die Sammlung von Stilen ab, zu denen dieser Stil gehört.

```csharp
public StyleCollection Styles { get; }
```

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

### Siehe auch

* class [StyleCollection](../../stylecollection/)
* class [Style](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
