---
title: HtmlLoadOptions.SupportVml
linktitle: SupportVml
articleTitle: SupportVml
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „HtmlLoadOptions SupportVml“ Ihr Web-Erlebnis verbessert, indem sie die VML-Bildunterstützung für eine verbesserte Grafikqualität aktiviert.
type: docs
weight: 70
url: /de/net/aspose.words.loading/htmlloadoptions/supportvml/
---
## HtmlLoadOptions.SupportVml property

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob VML-Bilder unterstützt werden sollen.

```csharp
public bool SupportVml { get; set; }
```

## Beispiele

Zeigt, wie bedingte Kommentare beim Laden eines HTML-Dokuments unterstützt werden.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Wenn der Wert wahr ist, berücksichtigen wir beim Parsen des geladenen Dokuments den VML-Code.
loadOptions.SupportVml = supportVml;

// Dieses Dokument enthält ein JPEG-Bild innerhalb der Tags "<!--[if gte vml 1]>",
// und ein anderes PNG-Bild innerhalb der Tags "<![if !vml]>".
// Wenn wir das Flag „SupportVml“ auf „true“ setzen, lädt Aspose.Words das JPEG.
// Wenn wir dieses Flag auf „false“ setzen, lädt Aspose.Words nur das PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Siehe auch

* class [HtmlLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
