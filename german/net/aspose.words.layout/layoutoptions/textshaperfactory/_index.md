---
title: LayoutOptions.TextShaperFactory
second_title: Aspose.Words für .NET-API-Referenz
description: LayoutOptions eigendom. Ruft ab oder legt festITextShaperFactory Implementierung die für erweiterte TypografieRenderingfunktionen verwendet wird.
type: docs
weight: 100
url: /de/net/aspose.words.layout/layoutoptions/textshaperfactory/
---
## LayoutOptions.TextShaperFactory property

Ruft ab oder legt fest[`ITextShaperFactory`](../../../aspose.words.shaping/itextshaperfactory/) Implementierung, die für erweiterte Typografie-Renderingfunktionen verwendet wird.

```csharp
public ITextShaperFactory TextShaperFactory { get; set; }
```

### Beispiele

Zeigt, wie OpenType-Funktionen mithilfe der HarfBuzz-Textformungs-Engine unterstützt werden.

```csharp
Document doc = new Document(MyDir + "OpenType text shaping.docx");

// Aspose.Words kann extern bereitgestellte Textformerobjekte verwenden,
// die Schriftarten darstellen und Forminformationen für Text berechnen.
// Für Dokumente, die mehrere Schriftarten verwenden, ist eine Textformerfabrik erforderlich.
// Wenn der Textformer werkseitig eingestellt ist, verwendet das Layout OpenType-Funktionen.
// Eine Instanzeigenschaft gibt ein statisches BasicTextShaperCache-Objekt zurück, das HarfBuzzTextShaperFactory umschließt.
doc.LayoutOptions.TextShaperFactory = HarfBuzzTextShaperFactory.Instance;

// Derzeit wird die Textformung beim Exportieren in PDF- oder XPS-Formate ausgeführt.
doc.Save(ArtifactsDir + "Document.OpenType.pdf");
```

### Siehe auch

* interface [ITextShaperFactory](../../../aspose.words.shaping/itextshaperfactory/)
* class [LayoutOptions](../)
* namensraum [Aspose.Words.Layout](../../layoutoptions/)
* Montage [Aspose.Words](../../../)


