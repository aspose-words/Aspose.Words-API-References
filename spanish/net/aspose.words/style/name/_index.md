---
title: Style.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words para .NET
description: Descubra la propiedad Nombre de estilo, administre y personalice fácilmente sus estilos para obtener una mejor flexibilidad de diseño y experiencia de usuario.
type: docs
weight: 130
url: /es/net/aspose.words/style/name/
---
## Style.Name property

Obtiene o establece el nombre del estilo.

```csharp
public string Name { get; set; }
```

## Observaciones

No puede ser una cadena vacía.

Si ya existe un estilo con ese nombre en la colección, este lo sobrescribirá. Todos los nodos afectados harán referencia al nuevo estilo.

## Ejemplos

Muestra cómo acceder a la colección de estilos de un documento.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// Enumerar y listar todos los estilos que un documento creado con Aspose.Words contiene de forma predeterminada.
using (IEnumerator<Style> stylesEnum = doc.Styles.GetEnumerator())
{
    while (stylesEnum.MoveNext())
    {
        Style curStyle = stylesEnum.Current;
        Console.WriteLine($"Style name:\t\"{curStyle.Name}\", of type \"{curStyle.Type}\"");
        Console.WriteLine($"\tSubsequent style:\t{curStyle.NextParagraphStyleName}");
        Console.WriteLine($"\tIs heading:\t\t\t{curStyle.IsHeading}");
        Console.WriteLine($"\tIs QuickStyle:\t\t{curStyle.IsQuickStyle}");

        Assert.AreEqual(doc, curStyle.Document);
    }
}
```

Muestra cómo clonar el estilo de un documento.

```csharp
Document doc = new Document();

// El método AddCopy crea una copia del estilo especificado y
// genera automáticamente un nuevo nombre para el estilo, como "Título 1_0".
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

// Utilice la propiedad "Nombre" del estilo para cambiar el nombre de identificación del estilo.
newStyle.Name = "My Heading 1";

//Nuestro documento ahora tiene dos estilos de aspecto idéntico con nombres diferentes.
// Cambiar la configuración de uno de los estilos no afecta al otro.
newStyle.Font.Color = Color.Red;

Assert.AreEqual("My Heading 1", newStyle.Name);
Assert.AreEqual("Heading 1", doc.Styles["Heading 1"].Name);

Assert.AreEqual(doc.Styles["Heading 1"].Type, newStyle.Type);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Name, newStyle.Font.Name);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Size, newStyle.Font.Size);
Assert.AreNotEqual(doc.Styles["Heading 1"].Font.Color, newStyle.Font.Color);
```

### Ver también

* class [Style](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
