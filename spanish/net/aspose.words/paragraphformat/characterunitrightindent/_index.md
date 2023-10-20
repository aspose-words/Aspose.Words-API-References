---
title: ParagraphFormat.CharacterUnitRightIndent
linktitle: CharacterUnitRightIndent
articleTitle: CharacterUnitRightIndent
second_title: Aspose.Words para .NET
description: ParagraphFormat CharacterUnitRightIndent propiedad. Obtiene o establece el valor de sangría correcta en caracteres para los párrafos especificados en C#.
type: docs
weight: 90
url: /es/net/aspose.words/paragraphformat/characterunitrightindent/
---
## ParagraphFormat.CharacterUnitRightIndent property

Obtiene o establece el valor de sangría correcta (en caracteres) para los párrafos especificados.

```csharp
public double CharacterUnitRightIndent { get; set; }
```

## Ejemplos

Muestra cómo cambiar el espaciado y la sangría de los párrafos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;

// A continuación se muestran cinco opciones de espaciado diferentes, junto con las propiedades a las que afecta indirectamente su configuración.
// 1 - Sangría izquierda:
Assert.AreEqual(format.LeftIndent, 0.0d);

format.CharacterUnitLeftIndent = 10.0;

Assert.AreEqual(format.LeftIndent, 120.0d);

// 2 - Sangría derecha:
Assert.AreEqual(format.RightIndent, 0.0d); 

format.CharacterUnitRightIndent = -5.5;

Assert.AreEqual(format.RightIndent, -66.0d);

// 3 - Sangría francesa:
Assert.AreEqual(format.FirstLineIndent, 0.0d);

format.CharacterUnitFirstLineIndent = 20.3;

Assert.AreEqual(format.FirstLineIndent, 243.59d, 0.1d);

// 4 - Interlineado antes de párrafos:
Assert.AreEqual(format.SpaceBefore, 0.0d);

format.LineUnitBefore = 5.1;

Assert.AreEqual(format.SpaceBefore, 61.1d, 0.1d);

// 5 - Interlineado después de párrafos:
Assert.AreEqual(format.SpaceAfter, 0.0d);

format.LineUnitAfter = 10.9;

Assert.AreEqual(format.SpaceAfter, 130.8d, 0.1d);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试" +
              "文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档测试文档");
```

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
