---
title: BuildingBlockGallery
second_title: Referencia de API de Aspose.Words para .NET
description: Especifica la galería predefinida en la que se clasifica un bloque de construcción.
type: docs
weight: 150
url: /es/net/aspose.words.buildingblocks/buildingblockgallery/
---
## BuildingBlockGallery enumeration

Especifica la galería predefinida en la que se clasifica un bloque de construcción.

```csharp
public enum BuildingBlockGallery
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| All | `0` | Especifica que esta entrada de documento del glosario se asociará con todos los valores de clasificación de galería posibles. |
| AutoText | `1` |  |
| Bibliography | `2` |  |
| CoverPage | `3` |  |
| CustomAutoText | `4` |  |
| CustomBibliography | `5` |  |
| CustomCoverPage | `6` |  |
| CustomEquations | `7` |  |
| CustomFooters | `8` |  |
| CustomHeaders | `9` |  |
| Custom1 | `10` |  |
| Custom2 | `11` |  |
| Custom3 | `12` |  |
| Custom4 | `13` |  |
| Custom5 | `14` |  |
| CustomPageNumber | `15` |  |
| CustomPageNumberAtBottom | `16` |  |
| CustomPageNumberAtMargin | `17` |  |
| CustomPageNumberAtTop | `18` |  |
| CustomQuickParts | `19` |  |
| CustomTableOfContents | `20` |  |
| CustomTables | `21` |  |
| CustomTextBox | `22` |  |
| CustomWatermarks | `23` |  |
| NoGallery | `24` |  |
| QuickParts | `25` |  |
| Equations | `26` |  |
| Footers | `27` |  |
| Headers | `28` |  |
| PageNumber | `29` |  |
| PageNumberAtBottom | `30` |  |
| PageNumberAtMargin | `31` |  |
| PageNumberAtTop | `32` |  |
| StructuredDocumentTagPlaceholderText | `33` |  |
| TableOfContents | `34` |  |
| Tables | `35` |  |
| TextBox | `36` |  |
| Watermarks | `37` |  |
| Default | `0` | Igual queAll . |

### Observaciones

corresponde a la **ST_DocPartGallery** escriba en OOXML.

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

* espacio de nombres [Aspose.Words.BuildingBlocks](../../aspose.words.buildingblocks/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
