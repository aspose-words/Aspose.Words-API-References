---
title: IStructuredDocumentTag.Placeholder
linktitle: Placeholder
articleTitle: Placeholder
second_title: Aspose.Words para .NET
description: Descubra la propiedad IStructuredDocumentTag Placeholder. Administre fácilmente el texto de marcador de posición para contenido SDT vacío y mejore la usabilidad de su documento.
type: docs
weight: 100
url: /es/net/aspose.words.markup/istructureddocumenttag/placeholder/
---
## IStructuredDocumentTag.Placeholder property

Obtiene el[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/) que contiene texto de marcador de posición que debe mostrarse cuando el contenido de esta ejecución SDT está vacío, el elemento XML mapeado asociado está vacío como se especifica mediante[`XmlMapping`](../xmlmapping/) elemento o el[`IsShowingPlaceholderText`](../isshowingplaceholdertext/) el elemento es verdadero.

```csharp
public BuildingBlock Placeholder { get; }
```

## Observaciones

Puede ser nulo, lo que significa que el marcador de posición no es aplicable para este Sdt.

## Ejemplos

Muestra cómo utilizar el contenido de un bloque de construcción como texto de marcador de posición personalizado para una etiqueta de documento estructurado.

```csharp
Document doc = new Document();

// Inserte una etiqueta de documento estructurado de texto plano del tipo "PlainText", que funcionará como un cuadro de texto.
// El contenido que se mostrará de forma predeterminada es un mensaje del tipo "Haga clic aquí para ingresar texto".
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

//Podemos hacer que la etiqueta muestre el contenido de un bloque de construcción en lugar del texto predeterminado.
// Primero, agregue un bloque de construcción con contenidos al documento de glosario.
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// Luego, use la propiedad "PlaceholderName" de la etiqueta del documento estructurado para hacer referencia a ese bloque de construcción por nombre.
tag.PlaceholderName = "Custom Placeholder";

// Si "PlaceholderName" hace referencia a un bloque existente en el documento de glosario del documento principal,
//Podremos verificar el bloque de construcción a través de la propiedad "Placeholder".
Assert.AreEqual(substituteBlock, tag.Placeholder);

// Establezca la propiedad "IsShowingPlaceholderText" en "verdadero" para tratar el
// Contenido actual de la etiqueta del documento estructurado como texto de marcador de posición.
// Esto significa que al hacer clic en el cuadro de texto en Microsoft Word se resaltará inmediatamente todo el contenido de la etiqueta.
// Establezca la propiedad "IsShowingPlaceholderText" en "falso" para obtener el
// etiqueta de documento estructurada para tratar su contenido como texto que un usuario ya ha ingresado.
// Al hacer clic en este texto en Microsoft Word, el cursor parpadeante se colocará en la ubicación donde se hizo clic.
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### Ver también

* class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* interface [IStructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
