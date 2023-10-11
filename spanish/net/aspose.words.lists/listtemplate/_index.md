---
title: Enum ListTemplate
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Lists.ListTemplate enumeración. Especifica uno de los formatos de lista predefinidos disponibles en Microsoft Word.
type: docs
weight: 3530
url: /es/net/aspose.words.lists/listtemplate/
---
## ListTemplate enumeration

Especifica uno de los formatos de lista predefinidos disponibles en Microsoft Word.

```csharp
public enum ListTemplate
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| BulletDefault | `0` | Lista con viñetas predeterminada con 9 niveles. La viñeta del primer nivel es un disco, la viñeta del segundo nivel es un círculo, la viñeta del tercer nivel es un cuadrado. Luego, el formato se repite para los niveles restantes. |
| BulletDisk | `0` | Igual queBulletDefault. |
| BulletCircle | `1` | La bala del primer nivel es un círculo. Los niveles restantes son los mismos que enBulletDefault. |
| BulletSquare | `2` | La bala del primer nivel es un cuadrado. Los niveles restantes son los mismos que enBulletDefault. |
| BulletDiamonds | `3` | La bala del primer nivel es un personaje Wingding de 4 diamantes. Los niveles restantes son los mismos que enBulletDefault. |
| BulletArrowHead | `4` | La bala del primer nivel es un personaje volador con punta de flecha. Los niveles restantes son los mismos que enBulletDefault. |
| BulletTick | `5` | La bala del primer nivel es un personaje Wingding. Los niveles restantes son los mismos que enBulletDefault. |
| NumberDefault | `6` | Lista numerada predeterminada con 9 niveles. Numeración arábiga (1., 2., 3., ...) para el primer nivel, numeración de letras minúsculas (a., b., c., ...) para el segundo nivel, numeración romana minúsculas (i ., ii., iii., ...) para el tercer nivel. Luego, el formato se repite para los niveles restantes. |
| NumberArabicDot | `6` | Igual queNumberDefault. |
| NumberArabicParenthesis | `7` | El número del primer nivel es "1)". Los niveles restantes son los mismos que enNumberDefault. |
| NumberUppercaseRomanDot | `8` | El número del primer nivel es "I". Los niveles restantes son los mismos que enNumberDefault. |
| NumberUppercaseLetterDot | `9` | El número del primer nivel es "A". Los niveles restantes son los mismos que enNumberDefault. |
| NumberLowercaseLetterParenthesis | `10` | El número del primer nivel es "a)". Los niveles restantes son los mismos que enNumberDefault. |
| NumberLowercaseLetterDot | `11` | El número del primer nivel es "a.". Los niveles restantes son los mismos que enNumberDefault. |
| NumberLowercaseRomanDot | `12` | El número del primer nivel es "i". Los niveles restantes son los mismos que enNumberDefault. |
| OutlineNumbers | `13` | Una lista esquemática con los niveles numerados "1), a), i), (1), (a), (i), 1., a., i.". |
| OutlineLegal | `14` | Una lista general con niveles está numerada como "1., 1.1., 1.1.1, ...". |
| OutlineBullets | `15` | Un esquema enumera varias viñetas para diferentes niveles. |
| OutlineHeadingsArticleSection | `16` | Una lista de esquema con niveles vinculados a estilos de título. |
| OutlineHeadingsLegal | `17` | Una lista de esquema con niveles vinculados a estilos de título. |
| OutlineHeadingsNumbers | `18` | Una lista de esquema con niveles vinculados a estilos de título. |
| OutlineHeadingsChapter | `19` | Una lista de esquema con niveles vinculados a estilos de título. |

### Observaciones

Un valor de plantilla de lista se utiliza como parámetro en the [`Add`](../listcollection/add/) método.

Las plantillas de lista Aspose.Words corresponden a las 21 plantillas de lista disponibles en el cuadro de diálogo Numeración y viñetas en Microsoft Word 2003.

### Ejemplos

Muestra cómo crear un documento que contenga todas las plantillas de lista de encabezados de esquema.

```csharp
public void OutlineHeadingTemplates()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    List list = doc.Lists.Add(ListTemplate.OutlineHeadingsArticleSection);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Article Section\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsLegal);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Legal\"");

    builder.InsertBreak(BreakType.PageBreak);

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsNumbers);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Numbers\"");

    list = doc.Lists.Add(ListTemplate.OutlineHeadingsChapter);
    AddOutlineHeadingParagraphs(builder, list, "Aspose.Words Outline - \"Chapters\"");

    doc.Save(ArtifactsDir + "Lists.OutlineHeadingTemplates.docx");
}

private static void AddOutlineHeadingParagraphs(DocumentBuilder builder, List list, string title)
{
    builder.ParagraphFormat.ClearFormatting();
    builder.Writeln(title);

    for (int i = 0; i < 9; i++)
    {
        builder.ListFormat.List = list;
        builder.ListFormat.ListLevelNumber = i;

        string styleName = "Heading " + (i + 1);
        builder.ParagraphFormat.StyleName = styleName;
        builder.Writeln(styleName);
    }

    builder.ListFormat.RemoveNumbers();
}
```

Muestra cómo reiniciar la numeración en una lista copiando una lista.

```csharp
Document doc = new Document();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
 // Podemos crear listas anidadas aumentando el nivel de sangría.
 // Podemos comenzar y finalizar una lista utilizando la propiedad "ListFormat" del generador de documentos.
// Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Cree una lista a partir de una plantilla de Microsoft Word y personalice su primer nivel de lista.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Aplicar nuestra lista a algunos párrafos.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Podemos agregar una copia de una lista existente a la colección de listas del documento
// para crear una lista similar sin realizar cambios en la original.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Aplicar la segunda lista a nuevos párrafos.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

Muestra cómo trabajar con niveles de lista.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
 // Podemos crear listas anidadas aumentando el nivel de sangría.
 // Podemos comenzar y finalizar una lista utilizando la propiedad "ListFormat" del generador de documentos.
// Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// A continuación se muestran dos tipos de listas que podemos crear usando un generador de documentos.
// 1 - Una lista numerada:
// Las listas numeradas crean un orden lógico para sus párrafos numerando cada elemento.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Al establecer la propiedad "ListLevelNumber", podemos aumentar el nivel de la lista
// para comenzar una sublista autónoma en el elemento de la lista actual.
// La plantilla de lista de Microsoft Word llamada "NumberDefault" usa números para crear niveles de lista para el primer nivel de lista.
 // Los niveles de lista más profundos utilizan letras y números romanos en minúscula.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Una lista con viñetas:
// Esta lista aplicará una sangría y un símbolo de viñeta ("•") antes de cada párrafo.
// Los niveles más profundos de esta lista utilizarán diferentes símbolos, como "■" y "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Podemos deshabilitar el formato de la lista para no formatear ningún párrafo posterior como lista al desactivar el indicador "Lista".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Lists](../../aspose.words.lists/)
* asamblea [Aspose.Words](../../)


