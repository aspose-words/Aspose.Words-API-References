---
title: CleanupOptions.UnusedLists
linktitle: UnusedLists
articleTitle: UnusedLists
second_title: Aspose.Words para .NET
description: Optimice sus documentos con la propiedad UnusedLists de CleanupOptions. Elimine fácilmente las listas y definiciones no utilizadas para un espacio de trabajo más limpio y eficiente.
type: docs
weight: 40
url: /es/net/aspose.words/cleanupoptions/unusedlists/
---
## CleanupOptions.UnusedLists property

Especifica si las listas y las definiciones de listas no utilizadas deben eliminarse del documento. El valor predeterminado es`verdadero` .

```csharp
public bool UnusedLists { get; set; }
```

## Ejemplos

Muestra cómo eliminar todos los estilos personalizados no utilizados de un documento.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// Combinado con los estilos incorporados, el documento ahora tiene ocho estilos.
// Un estilo personalizado se marca como "usado" mientras haya texto dentro del documento
// Formateado con ese estilo. Esto significa que los cuatro estilos que añadimos no se utilizan actualmente.
Assert.AreEqual(8, doc.Styles.Count);

// Aplicar un estilo de carácter personalizado y, a continuación, un estilo de lista personalizado. Al hacerlo, se marcarán como "usados".
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Ahora, hay un estilo de carácter sin uso y un estilo de lista sin uso.
// El método Cleanup(), cuando se configura con un objeto CleanupOptions, puede apuntar a estilos no utilizados y eliminarlos.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // Eliminar cada nodo al que se aplica un estilo personalizado lo marca nuevamente como "no utilizado".
// Vuelva a ejecutar el método Cleanup para eliminarlos.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### Ver también

* class [CleanupOptions](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
