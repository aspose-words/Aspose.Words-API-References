---
title: Run.PhoneticGuide
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words para .NET
description: Run PhoneticGuide propiedad. Obtiene unPhoneticGuide objeto en C#.
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
// Utiliza guía fonética en el texto asiático.
Assert.AreEqual(true, runs[0].IsPhoneticGuide);
Assert.AreEqual("base", runs[0].PhoneticGuide.BaseText);
Assert.AreEqual("ruby", runs[0].PhoneticGuide.RubyText);
```

### Ver también

* class [PhoneticGuide](../../phoneticguide/)
* class [Run](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
