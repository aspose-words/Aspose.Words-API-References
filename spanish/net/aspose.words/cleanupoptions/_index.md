---
title: CleanupOptions Class
linktitle: CleanupOptions
articleTitle: CleanupOptions
second_title: Aspose.Words para .NET
description: Aspose.Words.CleanupOptions clase. Permite especificar opciones para la limpieza de documentos en C#.
type: docs
weight: 210
url: /es/net/aspose.words/cleanupoptions/
---
## CleanupOptions class

Permite especificar opciones para la limpieza de documentos.

Para obtener más información, visite el[Limpiar un documento](https://docs.aspose.com/words/net/clean-up-a-document/) artículo de documentación.

```csharp
public class CleanupOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [CleanupOptions](cleanupoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DuplicateStyle](../../aspose.words/cleanupoptions/duplicatestyle/) { get; set; } | Obtiene/establece un indicador que indica si los estilos duplicados deben eliminarse del documento. El valor predeterminado es`FALSO` . |
| [UnusedBuiltinStyles](../../aspose.words/cleanupoptions/unusedbuiltinstyles/) { get; set; } | Especifica que no se utiliza[`BuiltIn`](../style/builtin/) Los estilos deben eliminarse del documento. |
| [UnusedLists](../../aspose.words/cleanupoptions/unusedlists/) { get; set; } | Especifica si la lista no utilizada y las definiciones de lista deben eliminarse del documento. El valor predeterminado es`verdadero` . |
| [UnusedStyles](../../aspose.words/cleanupoptions/unusedstyles/) { get; set; } | Especifica si los estilos no utilizados deben eliminarse del documento. El valor predeterminado es`verdadero` . |

## Ejemplos

Muestra cómo eliminar todos los estilos personalizados no utilizados de un documento.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// Combinado con los estilos integrados, el documento ahora tiene ocho estilos.
// Un estilo personalizado se marca como "usado" mientras haya texto dentro del documento
// formateado en ese estilo. Esto significa que los 4 estilos que agregamos no se utilizan actualmente.
Assert.AreEqual(8, doc.Styles.Count);

// Aplicar un estilo de carácter personalizado y luego un estilo de lista personalizado. Al hacerlo, se marcarán como "usados".
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Ahora hay un estilo de carácter no utilizado y un estilo de lista no utilizado.
// El método Cleanup(), cuando se configura con un objeto CleanupOptions, puede apuntar a estilos no utilizados y eliminarlos.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // Eliminar cada nodo al que se aplica un estilo personalizado lo marca como "no utilizado" nuevamente.
// Vuelva a ejecutar el método de limpieza para eliminarlos.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
