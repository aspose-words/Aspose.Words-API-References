---
title: FieldOptions.BuiltInTemplatesPaths
linktitle: BuiltInTemplatesPaths
articleTitle: BuiltInTemplatesPaths
second_title: Aspose.Words para .NET
description: Descubra cómo administrar las rutas de plantillas integradas de MS Word con la propiedad FieldOptions BuiltInTemplatesPaths para una creación de documentos sin problemas.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldoptions/builtintemplatespaths/
---
## FieldOptions.BuiltInTemplatesPaths property

Obtiene o establece rutas de plantillas integradas de MS Word.

```csharp
public string[] BuiltInTemplatesPaths { get; set; }
```

## Observaciones

Esta propiedad es utilizada por el[`FieldAutoText`](../../fieldautotext/) y[`FieldGlossary`](../../fieldglossary/) campos, si no se encuentra la entrada de texto automática referenciada en el[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) plantilla.

De forma predeterminada, MS Word almacena las plantillas integradas en los archivos c:\Users\&lt;nombre de usuario&gt;\AppData\Roaming\Microsoft\Document Building Blocks\1033\16\Built-In Building Blocks.dotx y C:\Users\&lt;nombre de usuario&gt;\AppData\Roaming\Microsoft\Templates\Normal.dotm.

## Ejemplos

Muestra cómo visualizar un bloque de construcción con campos AUTOTEXTO y GLOSARIO.

```csharp
Document doc = new Document();

// Cree un documento de glosario y agréguele un bloque de creación de Autotexto.
doc.GlossaryDocument = new GlossaryDocument();
BuildingBlock buildingBlock = new BuildingBlock(doc.GlossaryDocument);
buildingBlock.Name = "MyBlock";
buildingBlock.Gallery = BuildingBlockGallery.AutoText;
buildingBlock.Category = "General";
buildingBlock.Description = "MyBlock description";
buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;
doc.GlossaryDocument.AppendChild(buildingBlock);

// Crea una fuente y agrégala como texto a nuestro bloque de construcción.
Document buildingBlockSource = new Document();
DocumentBuilder buildingBlockSourceBuilder = new DocumentBuilder(buildingBlockSource);
buildingBlockSourceBuilder.Writeln("Hello World!");

Node buildingBlockContent = doc.GlossaryDocument.ImportNode(buildingBlockSource.FirstSection, true);
buildingBlock.AppendChild(buildingBlockContent);

// Establezca un archivo que contenga partes que nuestro documento o su plantilla adjunta pueden no contener.
doc.FieldOptions.BuiltInTemplatesPaths = new[] { MyDir + "Busniess brochure.dotx" };

DocumentBuilder builder = new DocumentBuilder(doc);

A continuación se muestran dos formas de utilizar campos para mostrar el contenido de nuestro bloque de construcción.
// 1 - Usando un campo AUTOTEXTO:
FieldAutoText fieldAutoText = (FieldAutoText)builder.InsertField(FieldType.FieldAutoText, true);
fieldAutoText.EntryName = "MyBlock";

Assert.AreEqual(" AUTOTEXT  MyBlock", fieldAutoText.GetFieldCode());

// 2 - Usando un campo GLOSARIO:
FieldGlossary fieldGlossary = (FieldGlossary)builder.InsertField(FieldType.FieldGlossary, true);
fieldGlossary.EntryName = "MyBlock";

Assert.AreEqual(" GLOSSARY  MyBlock", fieldGlossary.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.AUTOTEXT.GLOSSARY.dotx");
```

### Ver también

* class [FieldOptions](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
