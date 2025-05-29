---
title: ControlChar.Tab
linktitle: Tab
articleTitle: Tab
second_title: Aspose.Words para .NET
description: Descubra el campo de tabulación ControlChar, comprenda el carácter de tabulación x0009 para un formato de texto eficiente y una mejor gestión de datos.
type: docs
weight: 270
url: /es/net/aspose.words/controlchar/tab/
---
## ControlChar.Tab field

Carácter de tabulación: "\x0009" o "\t".

```csharp
public static readonly string Tab;
```

## Ejemplos

Muestra cómo establecer un intervalo personalizado para las posiciones de tabulación.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Establezca las tabulaciones para que aparezcan cada 72 puntos (1 pulgada).
builder.Document.DefaultTabStop = 72;

// Cada carácter de tabulación ajusta el texto posterior a la posición de tabulación más cercana.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Ver también

* class [ControlChar](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
