---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die LoadOptions LoadFormat-Eigenschaft, um Dokumentformate einfach festzulegen. Optimieren Sie das Laden mit der Standardeinstellung „Auto“ für reibungslose Leistung.
type: docs
weight: 90
url: /de/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

Gibt das Format des zu ladenden Dokuments an. Standard istAuto .

```csharp
public LoadFormat LoadFormat { get; set; }
```

## Bemerkungen

Es wird empfohlen, dass Sie dieAuto Wert und lassen Sie Aspose.Words das Dateiformat automatisch erkennen. Wenn Sie das Format des zu ladenden Dokuments kennen, können Sie das Format explizit angeben. Dadurch verkürzt sich die Ladezeit um den Mehraufwand für die automatische Formaterkennung. Wenn Sie ein explizites Ladeformat angeben und sich herausstellt, dass es falsch ist, wird die automatische Erkennung aufgerufen und ein zweiter Versuch zum Laden der Datei unternommen.

## Beispiele

Zeigt, wie beim Öffnen eines HTML-Dokuments eine Basis-URI angegeben wird.

```csharp
// Angenommen, wir möchten ein HTML-Dokument laden, das ein Bild enthält, das über eine relative URI verknüpft ist
// während sich das Bild an einem anderen Ort befindet. In diesem Fall müssen wir die relative URI in eine absolute auflösen.
    // Wir können eine Basis-URI mithilfe eines HtmlLoadOptions-Objekts bereitstellen.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Obwohl das Bild in der Eingabe-HTML beschädigt war, half uns unsere benutzerdefinierte Basis-URI, den Link zu reparieren.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Dieses Ausgabedokument zeigt das fehlende Bild an.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Siehe auch

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
