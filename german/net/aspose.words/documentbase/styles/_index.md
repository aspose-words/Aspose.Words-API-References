---
title: DocumentBase.Styles
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBase eigendom. Gibt eine Sammlung von Stilen zurück die im Dokument definiert sind.
type: docs
weight: 80
url: /de/net/aspose.words/documentbase/styles/
---
## DocumentBase.Styles property

Gibt eine Sammlung von Stilen zurück, die im Dokument definiert sind.

```csharp
public StyleCollection Styles { get; }
```

### Bemerkungen

Weitere Informationen finden Sie in der Beschreibung der[`StyleCollection`](../../stylecollection/) Klasse.

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

Zeigt, wie Sie ein Absatzformat mit Listenformatierung erstellen und verwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Einen benutzerdefinierten Absatzstil erstellen.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Erstellen Sie eine Liste und stellen Sie sicher, dass die Absätze, die diesen Stil verwenden, diese Liste verwenden.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Den Absatzstil auf den aktuellen Absatz des Document Builder anwenden und dann etwas Text hinzufügen.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Ändern Sie den Stil des Document Builder in einen Stil ohne Listenformatierung und schreiben Sie einen weiteren Absatz.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Siehe auch

* class [StyleCollection](../../stylecollection/)
* class [DocumentBase](../)
* namensraum [Aspose.Words](../../documentbase/)
* Montage [Aspose.Words](../../../)


