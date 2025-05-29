---
title: Style.BuiltIn
linktitle: BuiltIn
articleTitle: BuiltIn
second_title: Aspose.Words para .NET
description: Descubre si un estilo es una opción integrada en MS Word. ¡Mejora el diseño de tus documentos con nuestra guía completa sobre los estilos integrados de Word!
type: docs
weight: 40
url: /es/net/aspose.words/style/builtin/
---
## Style.BuiltIn property

Verdadero si este estilo es uno de los estilos integrados en MS Word.

```csharp
public bool BuiltIn { get; }
```

## Ejemplos

Muestra cómo diferenciar los estilos personalizados de los estilos integrados.

```csharp
Document doc = new Document();

// Cuando creamos un documento usando Microsoft Word, o programáticamente usando Aspose.Words,
//el documento vendrá con una colección de estilos para aplicar a su texto para modificar su apariencia.
//Podemos acceder a estos estilos incorporados a través de la colección "Estilos" del documento.
// Todos estos estilos tendrán el indicador "BuiltIn" establecido en "verdadero".
Style style = doc.Styles["Emphasis"];

Assert.True(style.BuiltIn);

// Crea un estilo personalizado y agrégalo a la colección.
 // Los estilos personalizados como este tendrán el indicador "BuiltIn" establecido en "falso".
style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Navy;
style.Font.Name = "Courier New";

Assert.False(style.BuiltIn);
```

### Ver también

* class [Style](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
