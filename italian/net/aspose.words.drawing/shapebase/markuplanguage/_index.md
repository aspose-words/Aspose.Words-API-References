---
title: ShapeBase.MarkupLanguage
linktitle: MarkupLanguage
articleTitle: MarkupLanguage
second_title: Aspose.Words per .NET
description: ShapeBase MarkupLanguage proprietà. Ottiene MarkupLanguage utilizzato per questo oggetto grafico in C#.
type: docs
weight: 390
url: /it/net/aspose.words.drawing/shapebase/markuplanguage/
---
## ShapeBase.MarkupLanguage property

Ottiene MarkupLanguage utilizzato per questo oggetto grafico.

```csharp
public ShapeMarkupLanguage MarkupLanguage { get; }
```

## Esempi

Mostra come verificare le dimensioni e il linguaggio di markup di una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Dml, shape.MarkupLanguage);
Assert.AreEqual(new SizeF(300, 300), shape.SizeInPoints);
```

### Guarda anche

* enum [ShapeMarkupLanguage](../../shapemarkuplanguage/)
* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
