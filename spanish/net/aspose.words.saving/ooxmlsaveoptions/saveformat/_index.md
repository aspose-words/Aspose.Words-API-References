---
title: OoxmlSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words para .NET
description: Descubra la propiedad SaveFormat de OoxmlSaveOptions para elegir fácilmente formatos de documentos como Docx, Docm, Dotx, Dotm o FlatOpc para guardar sin problemas.
type: docs
weight: 70
url: /es/net/aspose.words.saving/ooxmlsaveoptions/saveformat/
---
## OoxmlSaveOptions.SaveFormat property

Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Puede serDocx ,Docm , Dotx ,Dotm oFlatOpc .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OoxmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
