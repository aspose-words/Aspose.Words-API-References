---
title: ListLevel.DeletePictureBullet
linktitle: DeletePictureBullet
articleTitle: DeletePictureBullet
second_title: Aspose.Words für .NET
description: Entfernen Sie mühelos Bildaufzählungszeichen aus Ihrer aktuellen Listenebene mit der Methode „ListLevel DeletePictureBullet“. Vereinfachen Sie noch heute Ihre Dokumentformatierung!
type: docs
weight: 160
url: /de/net/aspose.words.lists/listlevel/deletepicturebullet/
---
## ListLevel.DeletePictureBullet method

Löscht das Bildaufzählungszeichen für die aktuelle Listenebene.

```csharp
public void DeletePictureBullet()
```

## Bemerkungen

Nach dem Löschen wird das Standardaufzählungszeichen angezeigt.

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
