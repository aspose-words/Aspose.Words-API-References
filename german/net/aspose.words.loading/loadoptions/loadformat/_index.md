---
title: LoadOptions.LoadFormat
linktitle: LoadFormat
articleTitle: LoadFormat
second_title: Aspose.Words für .NET
description: LoadOptions LoadFormat eigendom. Gibt das Format des zu ladenden Dokuments an. Standard istAuto  in C#.
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

Es wird empfohlen, dass Sie angebenAuto Geben Sie den Wert ein und lassen Sie Aspose.Words das Dateiformat automatisch erkennen. Wenn Sie das Format des Dokuments kennen, das Sie laden möchten, können Sie das Format explizit angeben. Dadurch wird die Ladezeit um den Mehraufwand, der mit der automatischen Formaterkennung verbunden ist, geringfügig verkürzt. Wenn Sie ein explizites Ladeformat angeben, wird es automatisch angezeigt Wenn sich herausstellt, dass die Datei falsch ist, wird die automatische Erkennung aufgerufen und ein zweiter Versuch unternommen, die Datei zu laden.

## Beispiele

Zeigt, wie man beim Öffnen eines HTML-Dokuments einen Basis-URI angibt.

```csharp
// Angenommen, wir möchten ein HTML-Dokument laden, das ein durch einen relativen URI verknüpftes Bild enthält
// während sich das Bild an einem anderen Ort befindet. In diesem Fall müssen wir den relativen URI in einen absoluten auflösen.
 // Wir können einen Basis-URI mithilfe eines HtmlLoadOptions-Objekts bereitstellen.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Während das Bild in der Eingabe-HTML-Datei defekt war, half uns unser benutzerdefinierter Basis-URI, den Link zu reparieren.
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
