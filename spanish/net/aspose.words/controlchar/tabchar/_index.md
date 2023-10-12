---
title: ControlChar.TabChar
second_title: Referencia de API de Aspose.Words para .NET
description: ControlChar campo. Carácter de tabulación char9 o t.
type: docs
weight: 280
url: /es/net/aspose.words/controlchar/tabchar/
---
## ControlChar.TabChar field

Carácter de tabulación: (char)9 o "\t".

```csharp
public const char TabChar;
```

### Ejemplos

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

* class [ControlChar](../)
* espacio de nombres [Aspose.Words](../../controlchar/)
* asamblea [Aspose.Words](../../../)


