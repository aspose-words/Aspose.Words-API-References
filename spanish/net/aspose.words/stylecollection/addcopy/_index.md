---
title: StyleCollection.AddCopy
linktitle: AddCopy
articleTitle: AddCopy
second_title: Aspose.Words para .NET
description: Copia estilos fácilmente con el método AddCopy de StyleCollection. ¡Mejora tu flujo de trabajo de diseño y optimiza la gestión de estilos hoy mismo!
type: docs
weight: 70
url: /es/net/aspose.words/stylecollection/addcopy/
---
## StyleCollection.AddCopy method

Copia un estilo en esta colección.

```csharp
public Style AddCopy(Style style)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| style | Style | Estilo a copiar. |

### Valor_devuelto

Estilo copiado listo para usar.

## Observaciones

El estilo a copiar puede pertenecer al mismo documento o a documentos diferentes.

Se copia el estilo vinculado.

Este método no copia los estilos base.

Si la colección ya contiene un estilo con el mismo nombre, entonces el nuevo nombre se genera automáticamente agregando el sufijo "_number" comenzando desde 0, por ejemplo, "Normal_0", "Encabezado 1_1", etc.[`Name`](../../style/name/) Configurador para cambiar el nombre del estilo importado.

## Ejemplos

Muestra cómo importar un estilo de un documento a otro documento diferente.

```csharp
Document srcDoc = new Document();

// Crea un estilo personalizado para el documento de origen.
Style srcStyle = srcDoc.Styles.Add(StyleType.Paragraph, "MyStyle");
srcStyle.Font.Color = Color.Red;

// Importa el estilo personalizado del documento de origen al documento de destino.
Document dstDoc = new Document();
Style newStyle = dstDoc.Styles.AddCopy(srcStyle);

//El estilo importado tiene una apariencia idéntica a su estilo de origen.
Assert.AreEqual("MyStyle", newStyle.Name);
Assert.AreEqual(Color.Red.ToArgb(), newStyle.Font.Color.ToArgb());
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

* class [Style](../../style/)
* class [StyleCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
