---
title: Font.HasDmlEffect
linktitle: HasDmlEffect
articleTitle: HasDmlEffect
second_title: Aspose.Words para .NET
description: Font HasDmlEffect método. Comprueba si se aplica un efecto de texto DrawingML particular en C#.
type: docs
weight: 560
url: /es/net/aspose.words/font/hasdmleffect/
---
## Font.HasDmlEffect method

Comprueba si se aplica un efecto de texto DrawingML particular.

```csharp
public bool HasDmlEffect(TextDmlEffect dmlEffectType)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| dmlEffectType | TextDmlEffect | Tipo de efecto de texto DrawingML. |

### Valor_devuelto

`verdadero` si se aplica un efecto de texto DrawingML particular.

## Ejemplos

Muestra cómo comprobar si una ejecución muestra un efecto de texto DrawingML.

```csharp
Document doc = new Document(MyDir + "DrawingML text effects.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.True(runs[0].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[1].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[2].Font.HasDmlEffect(TextDmlEffect.Reflection));
Assert.True(runs[3].Font.HasDmlEffect(TextDmlEffect.Effect3D));
Assert.True(runs[4].Font.HasDmlEffect(TextDmlEffect.Fill));
```

### Ver también

* enum [TextDmlEffect](../../textdmleffect/)
* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
