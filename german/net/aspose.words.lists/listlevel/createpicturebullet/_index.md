---
title: ListLevel.CreatePictureBullet
linktitle: CreatePictureBullet
articleTitle: CreatePictureBullet
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode „ListLevel CreatePictureBullet“, um Ihre Listen mühelos mit benutzerdefinierten Bildaufzählungszeichen zu verbessern und so für optische Attraktivität und Übersichtlichkeit zu sorgen.
type: docs
weight: 150
url: /de/net/aspose.words.lists/listlevel/createpicturebullet/
---
## ListLevel.CreatePictureBullet method

Erstellt eine Bildaufzählungsform für die aktuelle Listenebene.

```csharp
public void CreatePictureBullet()
```

## Bemerkungen

Bitte beachten Sie,[`NumberStyle`](../numberstyle/) wird eingestellt aufBullet und [`NumberFormat`](../numberformat/) zu "\xF0B7", um Bildaufzählungszeichen richtig anzuzeigen. Das rote Kreuzbild wird beim Erstellen als Bildaufzählungszeichen festgelegt. Um es zu ändern, verwenden Sie bitte[`ImageData`](../imagedata/).

## Beispiele

Zeigt, wie ein benutzerdefiniertes Bildsymbol für Listenelementbeschriftungen festgelegt wird.

```csharp
Document doc = new Document();

List list = doc.Lists.Add(ListTemplate.BulletCircle);

// Erstellen Sie ein Bildaufzählungszeichen für die aktuelle Listenebene und legen Sie ein Bild aus einem lokalen Dateisystem fest
// als Symbol, das die Aufzählungszeichen für diese Listenebene anzeigen.
list.ListLevels[0].CreatePictureBullet();
list.ListLevels[0].ImageData.SetImage(ImageDir + "Logo icon.ico");

Assert.IsTrue(list.ListLevels[0].ImageData.HasImage);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("Hello world!");
builder.Write("Hello again!");

doc.Save(ArtifactsDir + "Lists.CreatePictureBullet.docx");

list.ListLevels[0].DeletePictureBullet();

Assert.IsNull(list.ListLevels[0].ImageData);
```

### Siehe auch

* class [ListLevel](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
