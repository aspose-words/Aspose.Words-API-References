---
title: ChmLoadOptions
linktitle: ChmLoadOptions
articleTitle: ChmLoadOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie den ChmLoadOptions-Konstruktor für eine nahtlose Initialisierung. Legen Sie mühelos Standardwerte fest und verbessern Sie noch heute die Leistung Ihrer Anwendung!
type: docs
weight: 10
url: /de/net/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions constructor

Initialisiert eine neue Instanz dieser Klasse mit Standardwerten.

```csharp
public ChmLoadOptions()
```

## Beispiele

Zeigt, wie URLs wie „ms-its:myfile.chm::/index.htm“ aufgelöst werden.

```csharp
// Unser Dokument enthält URLs wie "ms-its:amhelp.chm::....htm", hat aber einen anderen Namen,
// daher funktionieren Dateilinks nach dem Speichern im HTML-Format nicht.
// Wir müssen den ursprünglichen Dateinamen in „ChmLoadOptions“ definieren, um dieses Verhalten zu vermeiden.
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### Siehe auch

* class [ChmLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
