---
title: Style.ParagraphFormat
linktitle: ParagraphFormat
articleTitle: ParagraphFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie auf die Absatzformatierung von Stilen zugreifen und diese anpassen können, um die Dokumentpräsentation zu verbessern und eine professionelle Formatierung zu erzielen.
type: docs
weight: 150
url: /de/net/aspose.words/style/paragraphformat/
---
## Style.ParagraphFormat property

Ruft die Absatzformatierung des Stils ab.

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

## Bemerkungen

Für Zeichen- und Listenstile gibt diese Eigenschaft zurück`null`.

## Beispiele

Zeigt, wie ein Absatzstil mit Listenformatierung erstellt und verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie einen benutzerdefinierten Absatzstil.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Erstellen Sie eine Liste und stellen Sie sicher, dass die Absätze, die diesen Stil verwenden, diese Liste verwenden.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Wenden Sie den Absatzstil auf den aktuellen Absatz des Dokumentgenerators an und fügen Sie dann etwas Text hinzu.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Ändern Sie den Stil des Dokument-Generators in einen Stil ohne Listenformatierung und schreiben Sie einen weiteren Absatz.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Siehe auch

* class [ParagraphFormat](../../paragraphformat/)
* class [Style](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
