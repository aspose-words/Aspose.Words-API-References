---
title: ShapeMarkupLanguage Enum
linktitle: ShapeMarkupLanguage
articleTitle: ShapeMarkupLanguage
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.ShapeMarkupLanguage, que define lenguajes de marcado de formas para mejorar el formato de los documentos y la flexibilidad del diseño.
type: docs
weight: 1670
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
| Vml | `1` | Se utiliza el lenguaje de marcado vectorial para definir la forma. |

## Ejemplos

Muestra cómo establecer una especificación de cumplimiento de OOXML para que la respete un documento guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si configuramos las opciones de compatibilidad para cumplir con Microsoft Word 2003,
// Insertar una imagen definirá su forma usando VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// El estándar OOXML "ISO/IEC 29500:2008" no admite formas VML.
// Si establecemos la propiedad "Compliance" del objeto SaveOptions en "OoxmlCompliance.Iso29500_2008_Strict",
 // cualquier documento que guardemos mientras pasamos este objeto tendrá que seguir ese estándar.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

//Nuestro documento guardado define la forma usando DML para cumplir con el estándar OOXML "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
