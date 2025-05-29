---
title: PhoneticGuide.BaseText
linktitle: BaseText
articleTitle: BaseText
second_title: Aspose.Words para .NET
description: Descubra la propiedad PhoneticGuide BaseText para acceder fácilmente y mejorar el texto base de la guía fonética para lograr una mayor claridad y comunicación.
type: docs
weight: 10
url: /es/net/aspose.words/phoneticguide/basetext/
---
## PhoneticGuide.BaseText property

Obtiene el texto base de la guía fonética.

```csharp
public string BaseText { get; }
```

## Ejemplos

Muestra cómo obtener propiedades de la guía fonética.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Utilice la guía fonética en el texto asiático.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);

PhoneticGuide phoneticGuide = runs[0].PhoneticGuide;
Assert.AreEqual("base", phoneticGuide.BaseText);
Assert.AreEqual("ruby", phoneticGuide.RubyText);
```

### Ver también

* class [PhoneticGuide](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
