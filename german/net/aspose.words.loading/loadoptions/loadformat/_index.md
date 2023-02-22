---
title: LoadOptions.LoadFormat
second_title: Aspose.Words für .NET-API-Referenz
description: LoadOptions eigendom. Gibt das Format des zu ladenden Dokuments an. Standard istAuto .
type: docs
weight: 90
url: /de/net/aspose.words.loading/loadoptions/loadformat/
---
## LoadOptions.LoadFormat property

Gibt das Format des zu ladenden Dokuments an. Standard istAuto .

```csharp
public LoadFormat LoadFormat { get; set; }
```

### Bemerkungen

Es wird empfohlen, die anzugebenAutoWert und lassen Sie Aspose.Words das Dateiformat automatisch erkennen . Wenn Sie das Format des Dokuments kennen, das Sie laden möchten, können Sie format explizit angeben und dies wird die Ladezeit durch den mit der automatischen Erkennung des Formats verbundenen Overhead etwas reduzieren. Wenn Sie ein explizites Ladeformat angeben, wird es sich umdrehen falsch ist, wird die automatische Erkennung aufgerufen und ein zweiter Versuch unternommen, die Datei zu laden.

### Beispiele

Zeigt, wie beim Öffnen eines HTML-Dokuments ein Basis-URI angegeben wird.

```csharp
// Angenommen, wir möchten ein .html-Dokument laden, das ein Bild enthält, das durch einen relativen URI verknüpft ist
// während sich das Bild an einem anderen Ort befindet. In diesem Fall müssen wir den relativen URI in einen absoluten auflösen.
 // Wir können einen Basis-URI mit einem HtmlLoadOptions-Objekt bereitstellen.
HtmlLoadOptions loadOptions = new HtmlLoadOptions(LoadFormat.Html, "", ImageDir);

Assert.AreEqual(LoadFormat.Html, loadOptions.LoadFormat);

Document doc = new Document(MyDir + "Missing image.html", loadOptions);

// Während das Bild in der Eingabe-.html-Datei beschädigt war, half uns unsere benutzerdefinierte Basis-URI, den Link zu reparieren.
Shape imageShape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];
Assert.True(imageShape.IsImage);

// Dieses Ausgabedokument zeigt das fehlende Bild an.
doc.Save(ArtifactsDir + "HtmlLoadOptions.BaseUri.docx");
```

### Siehe auch

* enum [LoadFormat](../../../aspose.words/loadformat/)
* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../loadoptions/)
* Montage [Aspose.Words](../../../)


