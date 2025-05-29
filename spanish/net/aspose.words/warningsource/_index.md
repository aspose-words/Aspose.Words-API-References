---
title: WarningSource Enum
linktitle: WarningSource
articleTitle: WarningSource
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.WarningSource, que identifica fuentes de advertencia durante la carga y el guardado de documentos para una mejor gestión de documentos.
type: docs
weight: 7500
url: /es/net/aspose.words/warningsource/
---
## WarningSource enumeration

Especifica el módulo que produce una advertencia durante la carga o el guardado del documento.

```csharp
public enum WarningSource
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Unknown | `0` | No se especificó la fuente de advertencia. |
| Layout | `1` | Módulo que crea un diseño de documento. |
| DrawingML | `2` | Módulo que renderiza formas DrawingML. |
| OfficeMath | `3` | Módulo que renderiza OfficeMath. |
| Shapes | `4` | Módulo que renderiza formas ordinarias. |
| Metafile | `5` | Módulo que renderiza metarchivos. |
| Xps | `6` | Módulo que renderiza XPS. |
| Pdf | `7` | Módulo que renderiza PDF. |
| Image | `8` | Módulo que renderiza imágenes. |
| Docx | `9` | Módulo que lee/escribe archivos DOCX. |
| Doc | `10` | Módulo que lee/escribe archivos DOC binarios. |
| Text | `11` | Módulo que lee/escribe archivos de texto plano. |
| Rtf | `12` | Módulo que lee/escribe archivos RTF. |
| WordML | `13` | Módulo que lee/escribe archivos WML. |
| Nrx | `14` | Módulos comunes que se comparten entre los módulos lectores/escritores DOCX/WML. |
| Odt | `15` | Módulo que lee/escribe archivos ODT. |
| Html | `16` | Módulo que lee/escribe archivos HTML/MHTML. |
| Validator | `17` | Módulo que verifica la consistencia y validez del modelo. |
| Xaml | `18` | Módulo que lee/escribe archivos Xaml. |
| Svm | `19` | Módulo que lee archivos Svm. |
| MathML | `20` | Módulo que lee archivos W3C MathML. |
| Font | `21` | Módulo que lee archivos de fuentes. |
| Svg | `22` | Módulo que lee archivos SVG. |
| Markdown | `23` | Módulo que lee/escribe archivos Markdown. |
| Chm | `24` | Módulo que lee archivos CHM. |
| Epub | `25` | Módulo que lee/escribe archivos EPUB. |
| Xml | `26` | Módulo que lee archivos XML. |
| Xlsx | `27` | Módulo que escribe archivos XLSX. |

## Ejemplos

Muestra cómo trabajar con la fuente de advertencia.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
