---
title: SaveOptions.PrettyFormat
linktitle: PrettyFormat
articleTitle: PrettyFormat
second_title: Aspose.Words para .NET
description: Mejore su salida con la propiedad PrettyFormat de SaveOptions. Actívela para obtener resultados más limpios y bien estructurados. El valor predeterminado es falso. ¡Descubra la diferencia!
type: docs
weight: 110
url: /es/net/aspose.words.saving/saveoptions/prettyformat/
---
## SaveOptions.PrettyFormat property

Cuando`verdadero` , formatos bonitos de salida donde corresponda. El valor predeterminado es`FALSO` .

```csharp
public bool PrettyFormat { get; set; }
```

## Observaciones

Empezar a`verdadero` para hacer que los archivos HTML, MHTML, EPUB, WordML, RTF, DOCX y ODT sean legibles para humanos. Útil para realizar pruebas o depurar.

## Ejemplos

Muestra cómo mejorar la legibilidad del código sin procesar de un documento .html guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

HtmlSaveOptions htmlOptions = new HtmlSaveOptions(SaveFormat.Html) { PrettyFormat = usePrettyFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.PrettyFormat.html", htmlOptions);

// Habilitar el formato bonito hace que el código HTML sin formato sea más legible al agregar tabulaciones y caracteres de nueva línea.
string html = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.PrettyFormat.html");
string newLine = Environment.NewLine;

if (usePrettyFormat)
    Assert.AreEqual(
        $"<html>{newLine}" +
                    $"\t<head>{newLine}" +
                        $"\t\t<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />{newLine}" +
                        $"\t\t<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />{newLine}" +
                        $"\t\t<meta name=\"generator\" content=\"{BuildVersionInfo.Product} {BuildVersionInfo.Version}\" />{newLine}" +
                        $"\t\t<title>{newLine}" +
                        $"\t\t</title>{newLine}" +
                    $"\t</head>{newLine}" +
                    $"\t<body style=\"font-family:'Times New Roman'; font-size:12pt\">{newLine}" +
                        $"\t\t<div>{newLine}" +
                            $"\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">{newLine}" +
                                $"\t\t\t\t<span>Hello world!</span>{newLine}" +
                            $"\t\t\t</p>{newLine}" +
                            $"\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">{newLine}" +
                                $"\t\t\t\t<span style=\"-aw-import:ignore\">&#xa0;</span>{newLine}" +
                            $"\t\t\t</p>{newLine}" +
                        $"\t\t</div>{newLine}" +
                    $"\t</body>{newLine}</html>", 
        html);
else
    Assert.AreEqual(
        "<html><head><meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />" +
                "<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />" +
                $"<meta name=\"generator\" content=\"{BuildVersionInfo.Product} {BuildVersionInfo.Version}\" /><title></title></head>" +
                "<body style=\"font-family:'Times New Roman'; font-size:12pt\">" +
                "<div><p style=\"margin-top:0pt; margin-bottom:0pt\"><span>Hello world!</span></p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\"><span style=\"-aw-import:ignore\">&#xa0;</span></p></div></body></html>", 
        html);
```

### Ver también

* class [SaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
