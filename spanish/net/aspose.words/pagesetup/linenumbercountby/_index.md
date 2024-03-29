---
title: PageSetup.LineNumberCountBy
linktitle: LineNumberCountBy
articleTitle: LineNumberCountBy
second_title: Aspose.Words para .NET
description: PageSetup LineNumberCountBy propiedad. Devuelve o establece el incremento numérico para los números de línea en C#.
type: docs
weight: 210
url: /es/net/aspose.words/pagesetup/linenumbercountby/
---
## PageSetup.LineNumberCountBy property

Devuelve o establece el incremento numérico para los números de línea.

```csharp
public int LineNumberCountBy { get; set; }
```

## Ejemplos

Muestra cómo habilitar la numeración de líneas para una sección.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Podemos usar el objeto PageSetup de la sección para mostrar números a la izquierda de las líneas de texto de la sección.
// Este es el mismo comportamiento que un objeto Lista,
// pero cubre toda la sección y no modifica el texto de ninguna manera.
// Nuestra sección reiniciará la numeración en cada nueva página desde 1 y mostrará el número,
// si es múltiplo de 3, a 50 puntos a la izquierda de la línea.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// El contador de líneas omitirá cualquier párrafo con el indicador "SuppressLineNumbers" establecido en "true".
// Este párrafo está en la línea 15, que es múltiplo de 3 y, por lo tanto, normalmente mostraría un número de línea.
// El contador de líneas de la sección también ignorará esta línea y tratará la siguiente línea como la 15.ª.
// y continuar el conteo desde ese punto en adelante.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### Ver también

* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
