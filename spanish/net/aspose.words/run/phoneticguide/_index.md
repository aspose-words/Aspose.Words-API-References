---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words para .NET
description: Consigue una pronunciación fluida con PhoneticGuide. Mejora tus habilidades lingüísticas y de comunicación accediendo a información fonética personalizada.
type: docs
weight: 40
url: /es/net/aspose.words/run/phoneticguide/
---
## Run.PhoneticGuide property

Obtiene un`PhoneticGuide` objeto.

```csharp
public PhoneticGuide PhoneticGuide { get; }
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

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
