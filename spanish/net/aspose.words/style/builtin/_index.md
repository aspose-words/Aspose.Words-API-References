---
title: BuiltIn
second_title: Referencia de API de Aspose.Words para .NET
description: Verdadero si este estilo es uno de los estilos incorporados en MS Word.
type: docs
weight: 30
url: /es/net/aspose.words/style/builtin/
---
## Style.BuiltIn property

Verdadero si este estilo es uno de los estilos incorporados en MS Word.

```csharp
public bool BuiltIn { get; }
```

### Ejemplos

Muestra cómo diferenciar los estilos personalizados de los estilos integrados.

```csharp
Document doc = new Document();

// Cuando creamos un documento usando Microsoft Word, o programáticamente usando Aspose.Words,
// el documento vendrá con una colección de estilos para aplicar a su texto para modificar su apariencia.
// Podemos acceder a estos estilos integrados a través de la colección "Estilos" del documento.
// Todos estos estilos tendrán el indicador "BuiltIn" establecido en "true".
Style style = doc.Styles["Emphasis"];

Assert.True(style.BuiltIn);

// Crea un estilo personalizado y añádelo a la colección.
  // Los estilos personalizados como este tendrán el indicador "BuiltIn" establecido en "falso".
style = doc.Styles.Add(StyleType.Character, "MyStyle");
style.Font.Color = Color.Navy;
style.Font.Name = "Courier New";

Assert.False(style.BuiltIn);
```

### Ver también

* class [Style](../../style)
* espacio de nombres [Aspose.Words](../../style)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
