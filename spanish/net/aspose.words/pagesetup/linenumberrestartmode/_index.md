---
title: PageSetup.LineNumberRestartMode
linktitle: LineNumberRestartMode
articleTitle: LineNumberRestartMode
second_title: Aspose.Words para .NET
description: Descubra la propiedad PageSetup LineNumberRestartMode para controlar la numeración de líneas elija entre reiniciar en nuevas páginas o numeración continua para documentos sin interrupciones.
type: docs
weight: 230
url: /es/net/aspose.words/pagesetup/linenumberrestartmode/
---
## PageSetup.LineNumberRestartMode property

Obtiene o establece la forma en que se ejecuta la numeración de líneas, es decir, si comienza de nuevo al principio de una nueva página o sección o se ejecuta de forma continua.

```csharp
public LineNumberRestartMode LineNumberRestartMode { get; set; }
```

## Ejemplos

Muestra cómo habilitar la numeración de líneas para una sección.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Podemos usar el objeto PageSetup de la sección para mostrar números a la izquierda de las líneas de texto de la sección.
// Este es el mismo comportamiento que un objeto Lista,
// pero cubre toda la sección y no modifica el texto de ninguna manera.
//Nuestra sección reiniciará la numeración en cada nueva página desde 1 y mostrará el número,
// si es múltiplo de 3, a 50pt a la izquierda de la línea.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// El contador de línea omitirá cualquier párrafo con el indicador "SuppressLineNumbers" establecido en "verdadero".
// Este párrafo está en la línea 15, que es un múltiplo de 3 y, por lo tanto, normalmente mostraría un número de línea.
// El contador de línea de la sección también ignorará esta línea, tratará la siguiente línea como la 15.
// y continuar el conteo desde ese punto en adelante.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### Ver también

* enum [LineNumberRestartMode](../../linenumberrestartmode/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
