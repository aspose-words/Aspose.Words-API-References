---
title: FieldGlossary.EntryName
linktitle: EntryName
articleTitle: EntryName
second_title: Aspose.Words para .NET
description: Descubra la propiedad EntryName de FieldGlossary para administrar fácilmente las entradas del glosario: obtenga o configure nombres para una integración perfecta del contenido.
type: docs
weight: 20
url: /es/net/aspose.words.fields/fieldglossary/entryname/
---
## FieldGlossary.EntryName property

Obtiene o establece el nombre de la entrada del glosario que se insertará.

```csharp
public string EntryName { get; set; }
```

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

* class [FieldGlossary](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
