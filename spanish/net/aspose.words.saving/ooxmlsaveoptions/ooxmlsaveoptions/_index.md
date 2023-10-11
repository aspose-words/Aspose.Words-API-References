---
title: OoxmlSaveOptions.OoxmlSaveOptions
second_title: Referencia de API de Aspose.Words para .NET
description: OoxmlSaveOptions constructor. Inicializa una nueva instancia de esta clase que se puede utilizar para guardar un documento en elDocx formato.
type: docs
weight: 10
url: /es/net/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions() {#constructor}

Inicializa una nueva instancia de esta clase que se puede utilizar para guardar un documento en elDocx formato.

```csharp
public OoxmlSaveOptions()
```

### Ejemplos

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

* class [OoxmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* asamblea [Aspose.Words](../../../)

---

## OoxmlSaveOptions(SaveFormat) {#constructor_1}

Inicializa una nueva instancia de esta clase que se puede utilizar para guardar un documento en elDocx , Docm ,Dotx ,Dotm o FlatOpc formato.

```csharp
public OoxmlSaveOptions(SaveFormat saveFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| saveFormat | SaveFormat | Puede serDocx ,Docm , Dotx ,Dotm oFlatOpc . |

### Ejemplos

Muestra cómo admitir caracteres de control heredados al convertir a .docx.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// Cuando guardamos el documento en formato OOXML, podemos crear un objeto OoxmlSaveOptions
// y luego pasarlo al método de guardado del documento para modificar cómo guardamos el documento.
// Establece la propiedad "KeepLegacyControlChars" en "true" para preservar
// el carácter heredado "ShortDateTime" mientras se guarda.
// Establece la propiedad "KeepLegacyControlChars" en "false" para eliminar
// el carácter heredado "ShortDateTime" del documento de salida.
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.AreEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f",
    doc.FirstSection.Body.GetText());
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OoxmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* asamblea [Aspose.Words](../../../)


