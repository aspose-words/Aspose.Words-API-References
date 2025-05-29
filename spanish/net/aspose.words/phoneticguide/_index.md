---
title: PhoneticGuide Class
linktitle: PhoneticGuide
articleTitle: PhoneticGuide
second_title: Aspose.Words para .NET
description: Descubre la clase Aspose.Words.PhoneticGuide para mejorar la legibilidad del texto con guías fonéticas. ¡Mejora la experiencia de usuario y la accesibilidad sin esfuerzo!
type: docs
weight: 5160
url: /es/net/aspose.words/phoneticguide/
---
## PhoneticGuide class

Representa la Guía Fonética.

```csharp
public class PhoneticGuide
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BaseText](../../aspose.words/phoneticguide/basetext/) { get; } | Obtiene el texto base de la guía fonética. |
| [RubyText](../../aspose.words/phoneticguide/rubytext/) { get; } | Obtiene el texto rubí de la guía fonética. |

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
