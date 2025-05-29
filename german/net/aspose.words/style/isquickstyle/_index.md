---
title: Style.IsQuickStyle
linktitle: IsQuickStyle
articleTitle: IsQuickStyle
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die IsQuickStyle-Eigenschaft Ihre MS Word-Erfahrung verbessert, indem sie Stile in der QuickStyle-Galerie für einfachen Zugriff und verbesserten Arbeitsablauf präsentiert.
type: docs
weight: 80
url: /de/net/aspose.words/style/isquickstyle/
---
## Style.IsQuickStyle property

Gibt an, ob dieser Stil in der Quick Style-Galerie in der MS Word-Benutzeroberfläche angezeigt wird.

```csharp
public bool IsQuickStyle { get; set; }
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

* class [Style](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
