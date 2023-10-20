---
title: Style Class
linktitle: Style
articleTitle: Style
second_title: Aspose.Words para .NET
description: Aspose.Words.Style clase. Representa un único estilo integrado o definido por el usuario en C#.
type: docs
weight: 6130
url: /es/net/aspose.words/style/
---
## Style class

Representa un único estilo integrado o definido por el usuario.

Para obtener más información, visite el[Trabajar con estilos y temas](https://docs.aspose.com/words/net/working-with-styles-and-themes/) artículo de documentación.

```csharp
public class Style
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Aliases](../../aspose.words/style/aliases/) { get; } | Obtiene todos los alias de este estilo. Si el estilo no tiene alias, se devuelve una matriz vacía de cadena. |
| [AutomaticallyUpdate](../../aspose.words/style/automaticallyupdate/) { get; set; } | Especifica si este estilo se redefine automáticamente en función del valor apropiado. |
| [BaseStyleName](../../aspose.words/style/basestylename/) { get; set; } | Obtiene/establece el nombre del estilo en el que se basa este estilo. |
| [BuiltIn](../../aspose.words/style/builtin/) { get; } | Verdadero si este estilo es uno de los estilos integrados en MS Word. |
| [Document](../../aspose.words/style/document/) { get; } | Obtiene el documento del propietario. |
| [Font](../../aspose.words/style/font/) { get; } | Obtiene el formato de caracteres del estilo. |
| [IsHeading](../../aspose.words/style/isheading/) { get; } | Verdadero cuando el estilo es uno de los estilos de título integrados. |
| [IsQuickStyle](../../aspose.words/style/isquickstyle/) { get; set; } | Especifica si este estilo se muestra en la galería de estilos rápidos dentro de la interfaz de usuario de MS Word. |
| [LinkedStyleName](../../aspose.words/style/linkedstylename/) { get; } | Obtiene el nombre del`Style` vinculado a éste. Devuelve una cadena vacía si no hay estilos vinculados. |
| [List](../../aspose.words/style/list/) { get; } | Obtiene la lista que define el formato de este estilo de lista. |
| [ListFormat](../../aspose.words/style/listformat/) { get; } | Proporciona acceso a las propiedades de formato de lista de un estilo de párrafo. |
| [Name](../../aspose.words/style/name/) { get; set; } | Obtiene o establece el nombre del estilo. |
| [NextParagraphStyleName](../../aspose.words/style/nextparagraphstylename/) { get; set; } | Obtiene/establece el nombre del estilo que se aplicará automáticamente a un nuevo párrafo insertado después de un párrafo formateado con el estilo especificado. |
| [ParagraphFormat](../../aspose.words/style/paragraphformat/) { get; } | Obtiene el formato de párrafo del estilo. |
| [StyleIdentifier](../../aspose.words/style/styleidentifier/) { get; } | Obtiene el identificador de estilo independiente de la configuración regional para un estilo integrado. |
| [Styles](../../aspose.words/style/styles/) { get; } | Obtiene la colección de estilos a la que pertenece este estilo. |
| [Type](../../aspose.words/style/type/) { get; } | Obtiene el tipo de estilo (párrafo o carácter). |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Equals](../../aspose.words/style/equals/#equals)(*Style*) | Se compara con el estilo especificado. Los estilos Istd se comparan solo para los estilos integrados. Los estilos predeterminados no se incluyen en la comparación. El estilo base, el estilo vinculado y el estilo del siguiente párrafo se comparan recursivamente. |
| [Remove](../../aspose.words/style/remove/)() | Elimina el estilo especificado del documento. |

## Ejemplos

Muestra cómo crear y utilizar un estilo de párrafo con formato de lista.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un estilo de párrafo personalizado.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Crea una lista y asegúrate de que los párrafos que usan este estilo usarán esta lista.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Aplique el estilo de párrafo al párrafo actual del creador de documentos y luego agregue algo de texto.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Cambie el estilo del creador de documentos a uno que no tenga formato de lista y escriba otro párrafo.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

Muestra cómo crear y aplicar un estilo personalizado.

```csharp
Document doc = new Document();

Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle");
style.Font.Name = "Times New Roman";
style.Font.Size = 16;
style.Font.Color = Color.Navy;
// Redefinir automáticamente el estilo.
style.AutomaticallyUpdate = true;

DocumentBuilder builder = new DocumentBuilder(doc);

// Aplicar uno de los estilos del documento al párrafo que está creando el creador del documento.
builder.ParagraphFormat.Style = doc.Styles["MyStyle"];
builder.Writeln("Hello world!");

Style firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

Assert.AreEqual(style, firstParagraphStyle);

// Elimina nuestro estilo personalizado de la colección de estilos del documento.
doc.Styles["MyStyle"].Remove();

firstParagraphStyle = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Style;

// Cualquier texto que utilizó un estilo eliminado vuelve al formato predeterminado.
Assert.False(doc.Styles.Any(s => s.Name == "MyStyle"));
Assert.AreEqual("Times New Roman", firstParagraphStyle.Font.Name);
Assert.AreEqual(12.0d, firstParagraphStyle.Font.Size);
Assert.AreEqual(Color.Empty.ToArgb(), firstParagraphStyle.Font.Color.ToArgb());
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
