---
title: ShapeMarkupLanguage Enum
linktitle: ShapeMarkupLanguage
articleTitle: ShapeMarkupLanguage
second_title: Aspose.Words para .NET
description: Aspose.Words.Drawing.ShapeMarkupLanguage enumeración. Especifica el lenguaje de marcado utilizado para la forma en C#.
type: docs
weight: 1280
url: /es/net/aspose.words.drawing/shapemarkuplanguage/
---
## ShapeMarkupLanguage enumeration

Especifica el lenguaje de marcado utilizado para la forma.

```csharp
public enum ShapeMarkupLanguage : byte
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Dml | `0` | El lenguaje de marcado de dibujo se utiliza para definir la forma. |
| Vml | `1` | El lenguaje de marcado vectorial se utiliza para definir la forma. |

## Ejemplos

Muestra cómo establecer una especificación de cumplimiento de OOXML para que se adhiera a un documento guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si configuramos opciones de compatibilidad para cumplir con Microsoft Word 2003,
// insertar una imagen definirá su forma usando VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// El estándar OOXML "ISO/IEC 29500:2008" no admite formas VML.
// Si configuramos la propiedad "Cumplimiento" del objeto SaveOptions en "OoxmlCompliance.Iso29500_2008_Strict",
 // cualquier documento que guardemos al pasar este objeto tendrá que seguir ese estándar.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Nuestro documento guardado define la forma usando DML para cumplir con el estándar OOXML "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
