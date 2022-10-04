---
title: VisitBuildingBlockStart
second_title: Referencia de API de Aspose.Words para .NET
description: Llamado cuando ha comenzado la enumeración de un bloque de creación.
type: docs
weight: 70
url: /es/net/aspose.words/documentvisitor/visitbuildingblockstart/
---
## DocumentVisitor.VisitBuildingBlockStart method

Llamado cuando ha comenzado la enumeración de un bloque de creación.

```csharp
public virtual VisitorAction VisitBuildingBlockStart(BuildingBlock block)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| block | BuildingBlock | El objeto que se está visitando. |

### Valor_devuelto

A[`VisitorAction`](../../visitoraction/) valor que especifica cómo continuar la enumeración.

### Observaciones

Nota: un nodo de bloque de creación y sus elementos secundarios no se visitan cuando ejecuta a Visitor sobre un[`Document`](../../document/) Si desea ejecutar un Visitante sobre un bloque de construcción , debe ejecutar el visitante sobre[`GlossaryDocument`](../../../aspose.words.buildingblocks/glossarydocument/) or llamar[`Accept`](../../../aspose.words.buildingblocks/buildingblock/accept/) .

### Ejemplos

Muestra formas de acceder a los componentes básicos en un documento de glosario.

```csharp
public void GlossaryDocument()
{
    Document doc = new Document();
    GlossaryDocument glossaryDoc = new GlossaryDocument();

    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 1" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 2" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 3" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 4" });
    glossaryDoc.AppendChild(new BuildingBlock(glossaryDoc) { Name = "Block 5" });

    Assert.AreEqual(5, glossaryDoc.BuildingBlocks.Count);

    doc.GlossaryDocument = glossaryDoc;

    // Hay varias formas de acceder a los bloques de construcción.
    // 1 - Obtener los primeros/últimos bloques de construcción de la colección:
    Assert.AreEqual("Block 1", glossaryDoc.FirstBuildingBlock.Name);
    Assert.AreEqual("Block 5", glossaryDoc.LastBuildingBlock.Name);

    // 2 - Obtener un bloque de construcción por índice:
    Assert.AreEqual("Block 2", glossaryDoc.BuildingBlocks[1].Name);
    Assert.AreEqual("Block 3", glossaryDoc.BuildingBlocks.ToArray()[2].Name);

    // 3 - Obtenga el primer bloque de construcción que coincida con una galería, nombre y categoría:
    Assert.AreEqual("Block 4", 
        glossaryDoc.GetBuildingBlock(BuildingBlockGallery.All, "(Empty Category)", "Block 4").Name);

    // Lo haremos usando un visitante personalizado,
    // que le dará a cada BuildingBlock en el GlossaryDocument un GUID único
    GlossaryDocVisitor visitor = new GlossaryDocVisitor();
    glossaryDoc.Accept(visitor);

    Console.WriteLine(visitor.GetText());

    // En Microsoft Word, podemos acceder a los bloques de construcción a través de "Insertar" -> "Piezas rápidas" -> "Organizador de bloques de construcción".
    doc.Save(ArtifactsDir + "BuildingBlocks.GlossaryDocument.dotx"); 
}

/// <summary>
/// Otorga a cada bloque de creación de un documento de glosario visitado un GUID único.
/// Almacena los pares de bloques de creación de GUID en un diccionario.
/// </summary>
public class GlossaryDocVisitor : DocumentVisitor
{
    public GlossaryDocVisitor()
    {
        mBlocksByGuid = new Dictionary<Guid, BuildingBlock>();
        mBuilder = new StringBuilder();
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    public Dictionary<Guid, BuildingBlock> GetDictionary()
    {
        return mBlocksByGuid;
    }

    public override VisitorAction VisitGlossaryDocumentStart(GlossaryDocument glossary)
    {
        mBuilder.AppendLine("Glossary document found!");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitGlossaryDocumentEnd(GlossaryDocument glossary)
    {
        mBuilder.AppendLine("Reached end of glossary!");
        mBuilder.AppendLine("BuildingBlocks found: " + mBlocksByGuid.Count);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockStart(BuildingBlock block)
    {
        block.Guid = Guid.NewGuid();
        mBlocksByGuid.Add(block.Guid, block);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitBuildingBlockEnd(BuildingBlock block)
    {
        mBuilder.AppendLine("\tVisited block \"" + block.Name + "\"");
        mBuilder.AppendLine("\t Type: " + block.Type);
        mBuilder.AppendLine("\t Gallery: " + block.Gallery);
        mBuilder.AppendLine("\t Behavior: " + block.Behavior);
        mBuilder.AppendLine("\t Description: " + block.Description);

        return VisitorAction.Continue;
    }

    private readonly Dictionary<Guid, BuildingBlock> mBlocksByGuid;
    private readonly StringBuilder mBuilder;
}
```

### Ver también

* enum [VisitorAction](../../visitoraction/)
* class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* class [DocumentVisitor](../)
* espacio de nombres [Aspose.Words](../../documentvisitor/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
