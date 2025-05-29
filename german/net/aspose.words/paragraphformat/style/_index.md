---
title: ParagraphFormat.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ParagraphFormat Style“, um den Absatzstil Ihres Dokuments einfach anzupassen und zu verbessern und so die Lesbarkeit und Präsentation zu verbessern.
type: docs
weight: 350
url: /de/net/aspose.words/paragraphformat/style/
---
## ParagraphFormat.Style property

Ruft den auf diese Formatierung angewendeten Absatzstil ab oder legt ihn fest.

```csharp
public Style Style { get; set; }
```

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

* class [Style](../../style/)
* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
