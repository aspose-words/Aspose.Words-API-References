---
title: Enum SdtType
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Markup.SdtType enumeración. Especifica el tipo de nodo de etiqueta de documento estructurado SDT.
type: docs
weight: 4040
url: /es/net/aspose.words.markup/sdttype/
---
## SdtType enumeration

Especifica el tipo de nodo de etiqueta de documento estructurado (SDT).

```csharp
public enum SdtType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | No se asigna ningún tipo al SDT. |
| Bibliography | `1` | El SDT representa una entrada de bibliografía. |
| Citation | `2` | El SDT representa una cita. |
| Equation | `3` | El SDT representa una ecuación. |
| DropDownList | `4` | El SDT representa una lista desplegable cuando se muestra en el documento. |
| ComboBox | `5` | El SDT representa un cuadro combinado cuando se muestra en el documento. |
| Date | `6` | El SDT representa un selector de fecha cuando se muestra en el documento. |
| BuildingBlockGallery | `7` | El SDT representa un tipo de galería de bloques de construcción. |
| DocPartObj | `8` | El SDT representa un tipo de parte del documento. |
| Group | `9` | El SDT representa una agrupación restringida cuando se muestra en el documento. |
| Picture | `10` | El SDT representa una imagen cuando se muestra en el documento. |
| RichText | `11` | El SDT representa un cuadro de texto enriquecido cuando se muestra en el documento. |
| PlainText | `12` | El SDT representa un cuadro de texto sin formato cuando se muestra en el documento. |
| Checkbox | `13` | El SDT representa una casilla de verificación cuando se muestra en el documento. |
| RepeatingSection | `14` | El SDT representa el tipo de sección repetida cuando se muestra en el documento. |
| RepeatingSectionItem | `15` | El SDT representa el elemento de sección repetido. |
| EntityPicker | `16` | El SDT representa un selector de entidades que permite al usuario seleccionar una instancia de un tipo de contenido externo. |

### Ejemplos

Muestra cómo crear una etiqueta de documento estructurado en grupo en el nivel de Fila.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();

// Crea una etiqueta de documento estructurado de grupo en el nivel de fila.
StructuredDocumentTag groupSdt = new StructuredDocumentTag(doc, SdtType.Group, MarkupLevel.Row);
table.AppendChild(groupSdt);
groupSdt.IsShowingPlaceholderText = false;
groupSdt.RemoveAllChildren();

// Crea una fila secundaria de la etiqueta del documento estructurado.
Row row = new Row(doc);
groupSdt.AppendChild(row);

Cell cell = new Cell(doc);
row.AppendChild(cell);

builder.EndTable();

// Insertar contenido de la celda.
cell.EnsureMinimum();
builder.MoveTo(cell.LastParagraph);
builder.Write("Lorem ipsum dolor.");

// Insertar texto después de la tabla.
builder.MoveTo(table.NextSibling);
builder.Write("Nulla blandit nisi.");

doc.Save(ArtifactsDir + "StructuredDocumentTag.SdtAtRowLevel.docx");
```

Muestra cómo trabajar con estilos para elementos de control de contenido.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran dos formas de aplicar un estilo del documento a una etiqueta de documento estructurado.
// 1 - Aplicar un objeto de estilo de la colección de estilos del documento:
Style quoteStyle = doc.Styles[StyleIdentifier.Quote];
StructuredDocumentTag sdtPlainText =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline) { Style = quoteStyle };

// 2 - Referencia a un estilo en el documento por nombre:
StructuredDocumentTag sdtRichText =
    new StructuredDocumentTag(doc, SdtType.RichText, MarkupLevel.Inline) { StyleName = "Quote" };

builder.InsertNode(sdtPlainText);
builder.InsertNode(sdtRichText);

Assert.AreEqual(NodeType.StructuredDocumentTag, sdtPlainText.NodeType);

NodeCollection tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

foreach (Node node in tags)
{
    StructuredDocumentTag sdt = (StructuredDocumentTag)node;

    Console.WriteLine(sdt.WordOpenXMLMinimal);

    Assert.AreEqual(StyleIdentifier.Quote, sdt.Style.StyleIdentifier);
    Assert.AreEqual("Quote", sdt.StyleName);
}
```

Muestra cómo llenar una tabla con datos de una parte XML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

CustomXmlPart xmlPart = doc.CustomXmlParts.Add("Books",
    "<books>" +
        "<book>" +
            "<title>Everyday Italian</title>" +
            "<author>Giada De Laurentiis</author>" +
        "</book>" +
        "<book>" +
            "<title>The C Programming Language</title>" +
            "<author>Brian W. Kernighan, Dennis M. Ritchie</author>" +
        "</book>" +
        "<book>" +
            "<title>Learning XML</title>" +
            "<author>Erik T. Ray</author>" +
        "</book>" +
    "</books>");

// Crea encabezados para datos del contenido XML.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Title");
builder.InsertCell();
builder.Write("Author");
builder.EndRow();
builder.EndTable();

// Crea una tabla con una sección repetida en su interior.
StructuredDocumentTag repeatingSectionSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSection, MarkupLevel.Row);
repeatingSectionSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book", string.Empty);
table.AppendChild(repeatingSectionSdt);

// Agregue un elemento de sección repetida dentro de la sección repetida y márquelo como una fila.
// Esta tabla tendrá una fila por cada elemento que podamos encontrar en el documento XML
// usando el XPath "/books[1]/book", de los cuales hay tres.
StructuredDocumentTag repeatingSectionItemSdt =
    new StructuredDocumentTag(doc, SdtType.RepeatingSectionItem, MarkupLevel.Row);
repeatingSectionSdt.AppendChild(repeatingSectionItemSdt);

Row row = new Row(doc);
repeatingSectionItemSdt.AppendChild(row);

// Asigna datos XML con celdas de tabla creadas para el título y autor de cada libro.
StructuredDocumentTag titleSdt =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Cell);
titleSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book[1]/title[1]", string.Empty);
row.AppendChild(titleSdt);

StructuredDocumentTag authorSdt =
    new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Cell);
authorSdt.XmlMapping.SetMapping(xmlPart, "/books[1]/book[1]/author[1]", string.Empty);
row.AppendChild(authorSdt);

doc.Save(ArtifactsDir + "StructuredDocumentTag.RepeatingSectionItem.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)


