---
title: Run.IsPhoneticGuide
linktitle: IsPhoneticGuide
articleTitle: IsPhoneticGuide
second_title: Aspose.Words para .NET
description: Descubra IsPhoneticGuide, una poderosa herramienta que determina si una secuencia sirve como guía fonética, mejorando la claridad y legibilidad de su texto.
type: docs
weight: 20
url: /es/net/aspose.words/run/isphoneticguide/
---
## Run.IsPhoneticGuide property

Obtiene un valor booleano que indica que la ejecución es una guía fonética.

```csharp
public bool IsPhoneticGuide { get; }
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

* class [Run](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
