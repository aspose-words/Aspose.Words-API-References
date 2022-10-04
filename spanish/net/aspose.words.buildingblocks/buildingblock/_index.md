---
title: BuildingBlock
second_title: Referencia de API de Aspose.Words para .NET
description: Representa una entrada de documento del glosario como un Building Block Autotexto o una entrada de Autocorrección.
type: docs
weight: 120
url: /es/net/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class

Representa una entrada de documento del glosario, como un Building Block, Autotexto o una entrada de Autocorrección.

```csharp
public class BuildingBlock : CompositeNode
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [BuildingBlock](buildingblock/)(GlossaryDocument) | Inicializa una nueva instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Behavior](../../aspose.words.buildingblocks/buildingblock/behavior/) { get; set; } | Especifica el comportamiento que se aplicará cuando el contenido del bloque de creación se inserte en el documento principal. |
| [Category](../../aspose.words.buildingblocks/buildingblock/category/) { get; set; } | Especifica la categorización de segundo nivel para el bloque de creación. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Obtiene todos los nodos secundarios inmediatos de este nodo. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Obtiene el número de hijos inmediatos de este nodo. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Especifica el identificador de nodo personalizado. |
| [Description](../../aspose.words.buildingblocks/buildingblock/description/) { get; set; } | Obtiene o establece la descripción asociada con este bloque de creación. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Obtiene el documento al que pertenece este nodo. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Obtiene el primer hijo del nodo. |
| [FirstSection](../../aspose.words.buildingblocks/buildingblock/firstsection/) { get; } | Obtiene la primera sección del bloque de creación. |
| [Gallery](../../aspose.words.buildingblocks/buildingblock/gallery/) { get; set; } | Especifica la categorización de primer nivel para el bloque de creación a efectos de la clasificación o la clasificación de la interfaz de usuario. |
| [Guid](../../aspose.words.buildingblocks/buildingblock/guid/) { get; set; } | Obtiene o establece un identificador (un GUID de 128 bits) que identifica de forma exclusiva este componente básico. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Devuelve verdadero si este nodo tiene nodos secundarios. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Devuelve verdadero ya que este nodo puede tener nodos secundarios. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Obtiene el último hijo del nodo. |
| [LastSection](../../aspose.words.buildingblocks/buildingblock/lastsection/) { get; } | Obtiene la última sección del bloque de creación. |
| [Name](../../aspose.words.buildingblocks/buildingblock/name/) { get; set; } | Obtiene o establece el nombre de este bloque de creación. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Obtiene el nodo que sigue inmediatamente a este nodo. |
| override [NodeType](../../aspose.words.buildingblocks/buildingblock/nodetype/) { get; } | Devuelve elBuildingBlock valor. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Obtiene el padre inmediato de este nodo. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Obtiene el nodo inmediatamente anterior a este nodo. |
| [Range](../../aspose.words/node/range/) { get; } | Devuelve un **Rango** objeto que representa la parte de un documento que está contenido en este nodo. |
| [Sections](../../aspose.words.buildingblocks/buildingblock/sections/) { get; } | Devuelve una colección que representa todas las secciones del bloque de creación. |
| [Type](../../aspose.words.buildingblocks/buildingblock/type/) { get; set; } | Especifica el tipo de bloque de creación. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Accept](../../aspose.words.buildingblocks/buildingblock/accept/)(DocumentVisitor) | Acepta un visitante. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Agrega el nodo especificado al final de la lista de nodos secundarios para este nodo. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicado del nodo. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reservado para uso del sistema. IXPathNavigable. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Obtiene el primer ancestro del especificado[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Obtiene el primer ancestro del tipo de objeto especificado. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Devuelve un enésimo nodo secundario que coincide con el tipo especificado. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Devuelve una colección activa de nodos secundarios que coinciden con el tipo especificado. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Proporciona soporte para la iteración de cada estilo sobre los nodos secundarios de este nodo. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Obtiene el texto de este nodo y de todos sus hijos. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Devuelve el índice del nodo secundario especificado en la matriz de nodos secundarios. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Inserta el nodo especificado inmediatamente después del nodo de referencia especificado. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Inserta el nodo especificado inmediatamente antes del nodo de referencia especificado. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Obtiene el siguiente nodo de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Agrega el nodo especificado al principio de la lista de nodos secundarios para este nodo. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Obtiene el nodo anterior de acuerdo con el algoritmo de recorrido del árbol de pedido previo. |
| [Remove](../../aspose.words/node/remove/)() | Se elimina a sí mismo del padre. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Elimina todos los nodos secundarios del nodo actual. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Elimina el nodo secundario especificado. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Elimina todo[`SmartTag`](../../aspose.words.markup/smarttag/) nodos descendientes del nodo actual. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Selecciona una lista de nodos que coinciden con la expresión XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Selecciona el primer nodo que coincide con la expresión XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exporta el contenido del nodo a una cadena en el formato especificado. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exporta el contenido del nodo a una cadena utilizando las opciones de guardado especificadas. |

### Observaciones

[`BuildingBlock`](./buildingblock/) solo puede contener[`Section`](../../aspose.words/section/) nodos.

[`BuildingBlock`](./buildingblock/) solo puede ser hijo de[`GlossaryDocument`](../glossarydocument/).

Puede crear nuevos bloques de construcción e insertarlos en un documento de glosario. Puede modificar o eliminar bloques de construcción existentes. Puede copiar o mover building blocks entre documentos. Puede insertar contenido de un bloque de creación en un documento.

corresponde a la **docPart** , **docPartPr** y **docPartBody**elementos en OOXML.

### Ejemplos

Muestra cómo agregar un bloque de creación personalizado a un documento.

```csharp
public void CreateAndInsert()
{
    // El glosario de un documento almacena bloques de construcción.
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();
    doc.GlossaryDocument = glossaryDoc;

    // Cree un bloque de creación, asígnele un nombre y luego agréguelo al documento del glosario.
    BuildingBlock block = new BuildingBlock(glossaryDoc)
    {
        Name = "Custom Block"
    };

    glossaryDoc.AppendChild(block);

    // Todos los GUID de bloques de creación nuevos tienen el mismo valor cero de forma predeterminada y podemos asignarles un nuevo valor único.
    Assert.AreEqual("00000000-0000-0000-0000-000000000000", block.Guid.ToString());

    block.Guid = Guid.NewGuid();

    // Las siguientes propiedades clasifican los bloques de construcción
    // en el menú podemos acceder en Microsoft Word mediante "Insertar" -> "Piezas rápidas" -> "Organizador de bloques de construcción".
    Assert.AreEqual("(Empty Category)", block.Category);
    Assert.AreEqual(BuildingBlockType.None, block.Type);
    Assert.AreEqual(BuildingBlockGallery.All, block.Gallery);
    Assert.AreEqual(BuildingBlockBehavior.Content, block.Behavior);

    // Antes de que podamos agregar este bloque de construcción a nuestro documento, necesitaremos darle algunos contenidos,
    // lo que haremos usando un visitante de documentos. Este visitante también establecerá una categoría, galería y comportamiento.
    BuildingBlockVisitor visitor = new BuildingBlockVisitor(glossaryDoc);
    block.Accept(visitor);

    // Podemos acceder al bloque que acabamos de hacer del documento del glosario.
    BuildingBlock customBlock = glossaryDoc.GetBuildingBlock(BuildingBlockGallery.QuickParts,
        "My custom building blocks", "Custom Block");

    // El bloque en sí es una sección que contiene el texto.
    Assert.AreEqual($"Text inside {customBlock.Name}\f", customBlock.FirstSection.Body.FirstParagraph.GetText());
    Assert.AreEqual(customBlock.FirstSection, customBlock.LastSection);

    // Ahora, podemos insertarlo en el documento como una nueva sección.
    doc.AppendChild(doc.ImportNode(customBlock.FirstSection, true));

    // También podemos encontrarlo en el Organizador de bloques de construcción de Microsoft Word y colocarlo manualmente.
    doc.Save(ArtifactsDir + "BuildingBlocks.CreateAndInsert.dotx");
}

/// <summary>
/// Configura un bloque de construcción visitado para insertarlo en el documento como una parte rápida y agrega texto a su contenido.
/// </summary>
public class BuildingBlockVisitor : DocumentVisitor
{
    public BuildingBlockVisitor(GlossaryDocument ownerGlossaryDoc)
    {
        mBuilder = new StringBuilder();
        mGlossaryDoc = ownerGlossaryDoc;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        // Configure el bloque de creación como una parte rápida y agregue propiedades utilizadas por el organizador de bloques de creación.
        block.Behavior = BuildingBlockBehavior.Paragraph;
        block.Category = "My custom building blocks";
        block.Description =
            "Using this block in the Quick Parts section of word will place its contents at the cursor.";
        block.Gallery = BuildingBlockGallery.QuickParts;

        // Agrega una sección con texto.
        // Insertar el bloque en el documento agregará esta sección con sus nodos secundarios en la ubicación.
        Section section = new Section(mGlossaryDoc);
        block.AppendChild(section);
        block.FirstSection.EnsureMinimum();

        Run run = new Run(mGlossaryDoc, "Text inside " + block.Name);
        block.FirstSection.Body.FirstParagraph.AppendChild(run);

        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.Append("Visited " + block.Name + "\r\n");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
    private readonly GlossaryDocument mGlossaryDoc;
}
```

### Ver también

* class [CompositeNode](../../aspose.words/compositenode/)
* espacio de nombres [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
