---
title: LoadOptions.BaseUri
linktitle: BaseUri
articleTitle: BaseUri
second_title: Aspose.Words für .NET
description: Entdecken Sie die LoadOptions BaseUri-Eigenschaft, um relative URIs in Ihren Dokumenten einfach in absolute umzuwandeln. Verbessern Sie noch heute Ihr URI-Management!
type: docs
weight: 20
url: /de/net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

Ruft die Zeichenfolge ab oder legt sie fest, die verwendet wird, um im Dokument gefundene relative URIs bei Bedarf in absolute URIs aufzulösen. Kann sein`null` oder leere Zeichenfolge. Standard ist`null` .

```csharp
public string BaseUri { get; set; }
```

## Bemerkungen

Diese Eigenschaft wird in den folgenden Fällen verwendet, um relative URIs in absolute aufzulösen:

1. Wenn ein HTML-Dokument aus einem Stream geladen wird und das Dokument Bilder mit relativen URIs vom Typ enthält und im HTML-Element BASE keine Basis-URI angegeben ist.
2. Beim Speichern eines Dokuments im PDF-Format oder in anderen Formaten können mithilfe relativer URIs verknüpfte Bilder abgerufen werden, damit die Bilder im Ausgabedokument gespeichert werden können.

## Beispiele

Zeigt, wie ein HTML-Dokument mit Bildern aus einem Stream unter Verwendung einer Basis-URI geöffnet wird.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Übergeben Sie die URI des Basisordners beim Laden
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
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
