---
title: HtmlSaveOptions.ExportCidUrlsForMhtmlResources
linktitle: ExportCidUrlsForMhtmlResources
articleTitle: ExportCidUrlsForMhtmlResources
second_title: Aspose.Words para .NET
description: Descubra cómo ExportCidUrlsForMhtmlResources de HtmlSaveOptions mejora los documentos MHTML al habilitar URLs CID para imágenes, fuentes y CSS. Valor predeterminado falso.
type: docs
weight: 110
url: /es/net/aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/
---
## HtmlSaveOptions.ExportCidUrlsForMhtmlResources property

Especifica si se deben usar URL con CID (Content-ID) para referenciar recursos (imágenes, fuentes, CSS) incluidos en documentos MHTML . El valor predeterminado es`FALSO` .

```csharp
public bool ExportCidUrlsForMhtmlResources { get; set; }
```

## Observaciones

Esta opción afecta únicamente a los documentos que se guardan en MHTML.

De manera predeterminada, los recursos en los documentos MHTML se referencian por nombre de archivo (por ejemplo, "image.png"), que se compara con los encabezados "Content-Location" de las partes MIME.

Esta opción habilita un método alternativo, donde las referencias a los archivos de recursos se escriben como URL CID (Content-ID) (por ejemplo, "cid:image.png") y se comparan con los encabezados "Content-ID".

En teoría, no debería haber diferencia entre los dos métodos de referencia y cualquiera de ellos debería funcionar correctamente en cualquier navegador o agente de correo. Sin embargo, en la práctica, algunos agentes no pueden recuperar recursos por nombre de archivo. Si su navegador o agente de correo se niega a cargar los recursos incluidos en un documento MTHML (no muestra imágenes o no carga estilos CSS), intente exportar el documento con URLs CID.

## Ejemplos

Muestra cómo habilitar identificadores de contenido para documentos MHTML de salida.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Al establecer esta bandera se reemplazarán las etiquetas "Content-Location"
// con etiquetas "Content-ID" para cada recurso del documento de entrada.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mhtml)
{
    ExportCidUrlsForMhtmlResources = exportCidUrlsForMhtmlResources,
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ContentIdUrls.mht", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ContentIdUrls.mht");

if (exportCidUrlsForMhtmlResources)
{
    Assert.True(outDocContents.Contains("Content-ID: <document.html>"));
    Assert.True(outDocContents.Contains("<link href=3D\"cid:styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    Assert.True(outDocContents.Contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
    Assert.True(outDocContents.Contains("<img src=3D\"cid:image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
else
{
    Assert.True(outDocContents.Contains("Content-Location: document.html"));
    Assert.True(outDocContents.Contains("<link href=3D\"styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    Assert.True(outDocContents.Contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
    Assert.True(outDocContents.Contains("<img src=3D\"image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
