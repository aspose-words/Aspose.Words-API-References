---
title: Style.NextParagraphStyleName
linktitle: NextParagraphStyleName
articleTitle: NextParagraphStyleName
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die Eigenschaft „NextParagraphStyleName“ effektiv nutzen können, um die Stilanwendung für neue Absätze zu automatisieren und so die Formatierung Ihres Dokuments zu verbessern.
type: docs
weight: 140
url: /de/net/aspose.words/style/nextparagraphstylename/
---
## Style.NextParagraphStyleName property

Ruft den Namen des Stils ab bzw. legt ihn fest, der automatisch auf einen neuen Absatz angewendet werden soll, der nach einem Absatz eingefügt wird, der mit dem angegebenen Stil formatiert ist.

```csharp
public string NextParagraphStyleName { get; set; }
```

## Bemerkungen

Diese Eigenschaft wird von Aspose.Words nicht verwendet. Der nächste Absatzstil wird erst automatisch angewendet, wenn Sie das Dokument in MS Word bearbeiten.

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
