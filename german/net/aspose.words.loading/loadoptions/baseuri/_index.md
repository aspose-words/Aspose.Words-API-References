---
title: LoadOptions.BaseUri
second_title: Aspose.Words für .NET-API-Referenz
description: LoadOptions eigendom. Ruft die Zeichenfolge ab oder legt diese fest die bei Bedarf zum Auflösen relativer URIs im Dokument in absolute URIs verwendet wird. Kann seinNull oder leere Zeichenfolge. Standard istNull .
type: docs
weight: 20
url: /de/net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

Ruft die Zeichenfolge ab oder legt diese fest, die bei Bedarf zum Auflösen relativer URIs im Dokument in absolute URIs verwendet wird. Kann sein`Null` oder leere Zeichenfolge. Standard ist`Null` .

```csharp
public string BaseUri { get; set; }
```

### Bemerkungen

Diese Eigenschaft wird verwendet, um in den folgenden Fällen relative URIs in absolute aufzulösen:

1. Wenn ein HTML-Dokument aus einem Stream geladen wird und das Dokument Bilder mit relativen URIs enthält und im BASE-HTML-Element kein Basis-URI angegeben ist.
2. Beim Speichern eines Dokuments im PDF- und anderen Format, um mit relativen URIs verknüpfte Bilder abzurufen, damit die Bilder im Ausgabedokument gespeichert werden können.

### Beispiele

Zeigt, wie man mithilfe eines Basis-URI ein HTML-Dokument mit Bildern aus einem Stream öffnet.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Beim Laden den URI des Basisordners übergeben
    // damit alle Bilder mit relativen URIs im HTML-Dokument gefunden werden können.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Überprüfen Sie, ob die erste Form des Dokuments ein gültiges Bild enthält.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Siehe auch

* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../loadoptions/)
* Montage [Aspose.Words](../../../)


