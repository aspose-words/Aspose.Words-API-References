---
title: ListFormat Class
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words para .NET
description: Domine el formato de listas en sus documentos con la clase Aspose.Words.Lists.ListFormat. Mejore fácilmente el estilo de los párrafos para una mejor legibilidad.
type: docs
weight: 3930
url: /es/net/aspose.words.lists/listformat/
---
## ListFormat class

Permite controlar qué formato de lista se aplica a un párrafo.

Para obtener más información, visite el[Trabajar con listas](https://docs.aspose.com/words/net/working-with-lists/) Artículo de documentación.

```csharp
public class ListFormat
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | Verdadero cuando al párrafo se le aplica formato de viñetas o numeración. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | Obtiene o establece la lista de la que este párrafo es miembro. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | Devuelve el formato de nivel de lista más cualquier modificación de formato aplicada al párrafo actual. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | Obtiene o establece el número de nivel de lista (0 a 8) para el párrafo. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | Inicia una nueva lista con viñetas predeterminada y la aplica al párrafo. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | Inicia una nueva lista numerada predeterminada y la aplica al párrafo. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | Aumenta el nivel de lista del párrafo actual en un nivel. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | Disminuye el nivel de lista del párrafo actual en un nivel. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | Elimina números o viñetas del párrafo actual y establece el nivel de lista en cero. |

## Observaciones

Un párrafo en un documento de Microsoft Word puede tener viñetas o numeración. Cuando un párrafo tiene viñetas o numeración, se dice que se aplica formato de lista al párrafo.

No creas objetos de la`ListFormat` clase directamente. Accedes`ListFormat`Como propiedad de otro objeto que puede tener formato de lista asociado. Actualmente, los objetos que pueden tener formato de lista son:[`Paragraph`](../../aspose.words/paragraph/) , [`Style`](../../aspose.words/style/) y[`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat` de un[`Paragraph`](../../aspose.words/paragraph/) especifica qué formato de lista y nivel de lista se aplica a ese párrafo en particular.

`ListFormat` de un[`Style`](../../aspose.words/style/) (aplicable solo a estilos de párrafo) permite especificar qué formato de lista y nivel de lista se aplica a todos los párrafos de ese estilo en particular.

`ListFormat` de un[`DocumentBuilder`](../../aspose.words/documentbuilder/) proporciona acceso al formato de la lista en la posición actual del cursor dentro de la[`DocumentBuilder`](../../aspose.words/documentbuilder/).

El formato de la lista en sí se almacena dentro de un[`List`](../list/) Objeto que se almacena por separado de los párrafos. Los objetos de lista se almacenan dentro de un[`ListCollection`](../listcollection/) Colección. Hay un single [`ListCollection`](../listcollection/) colección por[`Document`](../../aspose.words/document/).

Los párrafos no pertenecen físicamente a una lista. Los párrafos just hacen referencia a un objeto de lista específico mediante[`List`](./list/) propiedad y un nivel particular en la lista a través de la[`ListLevelNumber`](./listlevelnumber/) propiedad. Al configurar estas dos propiedades, usted controla qué viñetas y numeración se aplican a un párrafo.

## Ejemplos

Muestra cómo trabajar con niveles de lista.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
 //Podemos crear listas anidadas aumentando el nivel de sangría.
 // Podemos comenzar y finalizar una lista utilizando la propiedad "ListFormat" de un generador de documentos.
//Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
//A continuación se muestran dos tipos de listas que podemos crear usando un generador de documentos.
// 1 - Una lista numerada:
// Las listas numeradas crean un orden lógico para sus párrafos numerando cada elemento.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Al establecer la propiedad "ListLevelNumber", podemos aumentar el nivel de la lista
// para comenzar una sublista autónoma en el elemento de lista actual.
// La plantilla de lista de Microsoft Word llamada "NumberDefault" utiliza números para crear niveles de lista para el primer nivel de lista.
 // Los niveles de lista más profundos utilizan letras y números romanos en minúscula.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Una lista con viñetas:
//Esta lista aplicará una sangría y un símbolo de viñeta ("•") antes de cada párrafo.
// Los niveles más profundos de esta lista utilizarán símbolos diferentes, como "■" y "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Podemos deshabilitar el formato de lista para no formatear los párrafos subsiguientes como listas desmarcando la marca "Lista".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Lists](../../aspose.words.lists/)
* asamblea [Aspose.Words](../../)
