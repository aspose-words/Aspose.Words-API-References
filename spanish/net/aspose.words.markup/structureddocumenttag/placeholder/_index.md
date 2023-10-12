---
title: StructuredDocumentTag.Placeholder
second_title: Referencia de API de Aspose.Words para .NET
description: StructuredDocumentTag propiedad. Obtiene elBuildingBlockque contiene texto de marcador de posición que debe mostrarse cuando el contenido de esta ejecución de SDT está vacío el elemento XML asignado asociado está vacío como se especifica mediante elXmlMapping element o elIsShowingPlaceholderText elemento esverdadero .
type: docs
weight: 230
url: /es/net/aspose.words.markup/structureddocumenttag/placeholder/
---
## StructuredDocumentTag.Placeholder property

Obtiene el[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/)que contiene texto de marcador de posición que debe mostrarse cuando el contenido de esta ejecución de SDT está vacío, el elemento XML asignado asociado está vacío como se especifica mediante el[`XmlMapping`](../xmlmapping/) element o el[`IsShowingPlaceholderText`](../isshowingplaceholdertext/) elemento es`verdadero` .

```csharp
public BuildingBlock Placeholder { get; }
```

### Observaciones

Puede ser`nulo`, lo que significa que el marcador de posición no es aplicable a este SDT.

### Ejemplos

Muestra cómo utilizar el contenido de un bloque de creación como texto de marcador de posición personalizado para una etiqueta de documento estructurado.

```csharp
Document doc = new Document();

// Inserta una etiqueta de documento estructurado de texto plano del tipo "PlainText", que funcionará como un cuadro de texto.
// El contenido que mostrará de forma predeterminada es "Haga clic aquí para ingresar texto". inmediato.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Podemos hacer que la etiqueta muestre el contenido de un bloque de construcción en lugar del texto predeterminado.
// Primero, agregue un bloque de construcción con contenido al documento del glosario.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// Luego, use la propiedad "PlaceholderName" de la etiqueta del documento estructurado para hacer referencia a ese bloque de construcción por su nombre.
tag.PlaceholderName = "Custom Placeholder";

// Si "PlaceholderName" se refiere a un bloque existente en el glosario del documento principal,
// podremos verificar el bloque de construcción mediante la propiedad "Marcador de posición".
Assert.AreEqual(substituteBlock, tag.Placeholder);

// Establece la propiedad "IsShowingPlaceholderText" en "true" para tratar el
// contenido actual de la etiqueta del documento estructurado como texto de marcador de posición.
// Esto significa que al hacer clic en el cuadro de texto en Microsoft Word se resaltará inmediatamente todo el contenido de la etiqueta.
// Establece la propiedad "IsShowingPlaceholderText" en "false" para obtener el
// etiqueta de documento estructurada para tratar su contenido como texto que un usuario ya ha ingresado.
// Al hacer clic en este texto en Microsoft Word, se colocará el cursor parpadeante en la ubicación en la que se hizo clic.
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### Ver también

* class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../structureddocumenttag/)
* asamblea [Aspose.Words](../../../)


