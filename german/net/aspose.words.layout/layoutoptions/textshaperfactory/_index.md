---
title: LayoutOptions.TextShaperFactory
linktitle: TextShaperFactory
articleTitle: TextShaperFactory
second_title: Aspose.Words für .NET
description: Entdecken Sie die TextShaperFactory-Eigenschaft LayoutOptions für erweiterte Typografie. Verbessern Sie Ihr Rendering mit anpassbaren ITextShaperFactory-Implementierungen.
type: docs
weight: 100
url: /de/net/aspose.words.layout/layoutoptions/textshaperfactory/
---
## LayoutOptions.TextShaperFactory property

Ruft ab oder legt fest[`ITextShaperFactory`](../../../aspose.words.shaping/itextshaperfactory/) Implementierung, die für erweiterte Typografie-Rendering-Funktionen verwendet wird.

```csharp
public ITextShaperFactory TextShaperFactory { get; set; }
```

## Beispiele

Zeigt, wie OpenType-Funktionen mithilfe der Textgestaltungs-Engine von HarfBuzz unterstützt werden.

```csharp
Document doc = new Document(MyDir + "OpenType text shaping.docx");

// Aspose.Words kann extern bereitgestellte Text Shaper-Objekte verwenden,
// die Schriftarten darstellen und Forminformationen für Text berechnen.
// Für Dokumente, die mehrere Schriftarten verwenden, ist eine Text Shaper Factory erforderlich.
// Wenn der Text Shaper werkseitig eingestellt ist, verwendet das Layout OpenType-Funktionen.
// Eine Instanzeigenschaft gibt ein statisches BasicTextShaperCache-Objekt zurück, das HarfBuzzTextShaperFactory umschließt.
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

// Derzeit wird die Textformung beim Exportieren in die Formate PDF oder XPS durchgeführt.
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### Siehe auch

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
