---
title: Document.DefaultTabStop
linktitle: DefaultTabStop
articleTitle: DefaultTabStop
second_title: Aspose.Words para .NET
description: Document DefaultTabStop propiedad. Obtiene o establece el intervalo en puntos entre las tabulaciones predeterminadas en C#.
type: docs
weight: 90
url: /es/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

Obtiene o establece el intervalo (en puntos) entre las tabulaciones predeterminadas.

```csharp
public double DefaultTabStop { get; set; }
```

## Ejemplos

Muestra cómo establecer un intervalo personalizado para las posiciones de tabulación.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Establece tabulaciones para que aparezcan cada 72 puntos (1 pulgada).
builder.Document.DefaultTabStop = 72;

// Cada carácter de tabulación ajusta el texto posterior a la siguiente posición de tabulación más cercana.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Ver también

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
