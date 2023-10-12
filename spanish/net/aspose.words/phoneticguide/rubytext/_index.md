---
title: PhoneticGuide.RubyText
second_title: Referencia de API de Aspose.Words para .NET
description: PhoneticGuide propiedad. Obtiene el texto rubí de la guía fonética.
type: docs
weight: 20
url: /es/net/aspose.words/phoneticguide/rubytext/
---
## PhoneticGuide.RubyText property

Obtiene el texto rubí de la guía fonética.

```csharp
public string RubyText { get; }
```

### Ejemplos

Muestra cómo obtener propiedades de la guía fonética.

```csharp
Document doc = new Document(MyDir + "Phonetic guide.docx");            

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;
// Utiliza guía fonética en el texto asiático.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);
Assert.AreEqual("base", runs[0].PhoneticGuide.BaseText);
Assert.AreEqual("ruby", runs[0].PhoneticGuide.RubyText);
```

### Ver también

* class [PhoneticGuide](../)
* espacio de nombres [Aspose.Words](../../phoneticguide/)
* asamblea [Aspose.Words](../../../)


