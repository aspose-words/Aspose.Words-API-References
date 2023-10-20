---
title: SaveOptions.PrettyFormat
linktitle: PrettyFormat
articleTitle: PrettyFormat
second_title: Aspose.Words para .NET
description: SaveOptions PrettyFormat propiedad. cuandoverdadero salida con bonitos formatos cuando corresponda. El valor predeterminado esFALSO  en C#.
type: docs
weight: 110
url: /es/net/aspose.words.saving/saveoptions/prettyformat/
---
## SaveOptions.PrettyFormat property

cuando`verdadero` salida con bonitos formatos cuando corresponda. El valor predeterminado es`FALSO` .

```csharp
public bool PrettyFormat { get; set; }
```

## Observaciones

Ajustado a`verdadero` para hacer que los resultados HTML, MHTML, EPUB, WordML, RTF, DOCX y ODT sean legibles para humanos. Útil para pruebas o depuración.

## Ejemplos

Muestra cómo mejorar la legibilidad del código sin formato de un documento .html guardado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

HtmlSaveOptions htmlOptions = new HtmlSaveOptions(SaveFormat.Html) { PrettyFormat = usePrettyFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.PrettyFormat.html", htmlOptions);

// Habilitar el formato bonito hace que el código HTML sin formato sea más legible al agregar tabulaciones y caracteres de nueva línea.
string html = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.PrettyFormat.html");

if (usePrettyFormat)
    Assert.AreEqual(
        "<html>\r\n" +
                    "\t<head>\r\n" +
                        "\t\t<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\" />\r\n" +
                        "\t\t<meta http-equiv=\"Content-Style-Type\" content=\"text/css\" />\r\n" +
                        $"\t\t<meta name=\"generator\" content=\"{BuildVersionInfo.Product} {BuildVersionInfo.Version}\" />\r\n" +
                        "\t\t<title>\r\n" +
                        "\t\t</title>\r\n" +
                    "\t</head>\r\n" +
                    "\t<body style=\"font-family:'Times New Roman'; font-size:12pt\">\r\n" +
                        "\t\t<div>\r\n" +
                            "\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">\r\n" +
                                "\t\t\t\t<span>Hello world!</span>\r\n" +
                            "\t\t\t</p>\r\n" +
                            "\t\t\t<p style=\"margin-top:0pt; margin-bottom:0pt\">\r\n" +
                                "\t\t\t\t<span style=\"-aw-import:ignore\">&#xa0;</span>\r\n" +
                            "\t\t\t</p>\r\n" +
                        "\t\t</div>\r\n" +
                    "\t</body>\r\n</html>", 
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
