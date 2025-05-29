---
title: PhoneticGuide.RubyText
linktitle: RubyText
articleTitle: RubyText
second_title: Aspose.Words para .NET
description: Descubra la propiedad PhoneticGuide RubyText para acceder y mejorar el texto rubí para una mayor claridad fonética en sus aplicaciones.
type: docs
weight: 20
url: /es/net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

Obtiene el texto rubí de la guía fonética.

```csharp
public string RubyText { get; }
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
