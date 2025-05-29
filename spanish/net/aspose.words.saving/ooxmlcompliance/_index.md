---
title: OoxmlCompliance Enum
linktitle: OoxmlCompliance
articleTitle: OoxmlCompliance
second_title: Aspose.Words para .NET
description: Explora la enumeración Aspose.Words.Saving.OoxmlCompliance para elegir tu especificación OOXML preferida y optimizar el guardado en formato DOCX. ¡Mejora la calidad de tus documentos hoy mismo!
type: docs
weight: 6120
url: /es/net/aspose.words.saving/ooxmlcompliance/
---
## OoxmlCompliance enumeration

Permite especificar qué especificación OOXML se utilizará al guardar en formato DOCX.

```csharp
public enum OoxmlCompliance
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Ecma376_2006 | `0` | ECMA-376 1.ª edición, 2006. |
| Iso29500_2008_Transitional | `1` | ISO/IEC 29500:2008 Nivel de cumplimiento transitorio. |
| Iso29500_2008_Strict | `2` | ISO/IEC 29500:2008 Nivel de cumplimiento estricto. |

## Ejemplos

Muestra cómo insertar formas DML en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//A continuación se muestran dos tipos de envoltura que pueden tener las formas.
// 1 - Flotante:
builder.InsertShape(ShapeType.TopCornersRounded, RelativeHorizontalPosition.Page, 100,
        RelativeVerticalPosition.Page, 100, 50, 50, WrapType.None);

// 2 - En línea:
builder.InsertShape(ShapeType.DiagonalCornersRounded, 50, 50);

// Si necesita crear formas "no primitivas", como SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
// EsquinasSuperioresUnaRedondeadaUnaRecortada, EsquinaSimpleRedondeada, EsquinasSuperioresRedondeadas o EsquinasDiagonalesRedondeadas
// luego guarde el documento con cumplimiento "Estricto" o "Transicional", lo que permite guardar la forma como DML.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.Compliance = OoxmlCompliance.Iso29500_2008_Transitional;

doc.Save(ArtifactsDir + "Shape.ShapeInsertion.docx", saveOptions);
```

Muestra cómo configurar una lista para reiniciar la numeración en cada sección.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

doc.Lists.Add(ListTemplate.NumberDefault);

Aspose.Words.Lists.List list = doc.Lists[0];
list.IsRestartAtEachSection = restartListAtEachSection;

// La propiedad "IsRestartAtEachSection" solo será aplicable cuando
// El nivel de cumplimiento OOXML del documento corresponde a un estándar más reciente que "OoxmlComplianceCore.Ecma376".
OoxmlSaveOptions options = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Transitional
};

builder.ListFormat.List = list;

builder.Writeln("List item 1");
builder.Writeln("List item 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("List item 3");
builder.Writeln("List item 4");

doc.Save(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx", options);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.RestartingDocumentList.docx");

Assert.AreEqual(restartListAtEachSection, doc.Lists[0].IsRestartAtEachSection);
```

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
