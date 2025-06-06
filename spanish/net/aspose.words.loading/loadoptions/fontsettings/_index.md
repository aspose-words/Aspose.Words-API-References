---
title: LoadOptions.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words para .NET
description: Personaliza la configuración de fuentes de tu documento con LoadOptions FontSettings para mejorar la legibilidad y el estilo. ¡Optimiza tus documentos sin esfuerzo!
type: docs
weight: 60
url: /es/net/aspose.words.loading/loadoptions/fontsettings/
---
## LoadOptions.FontSettings property

Permite especificar la configuración de fuentes del documento.

```csharp
public FontSettings FontSettings { get; set; }
```

## Observaciones

Al cargar algunos formatos, Aspose.Words puede requerir la resolución de las fuentes. Por ejemplo, al cargar documentos HTML, Aspose.Words puede resolver las fuentes para realizar un reemplazo de fuentes.

Si se establece en`nulo` , configuración de fuente estática predeterminada[`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) se utilizará.

El valor predeterminado es`nulo`.

## Ejemplos

Muestra cómo aplicar configuraciones de sustitución de fuentes al cargar un documento.

```csharp
// Crea un objeto FontSettings que sustituirá la fuente "Times New Roman"
// con la fuente "Arvo" de nuestra carpeta "MyFonts".
FontSettings fontSettings = new FontSettings();
fontSettings.SetFontsFolder(FontsDir, false);
fontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Times New Roman", "Arvo");

// Establezca ese objeto FontSettings como una propiedad de un objeto LoadOptions recién creado.
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = fontSettings;

// Cargue el documento y luego renderícelo como PDF con la sustitución de fuente.
Document doc = new Document(MyDir + "Document.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.FontSettings.pdf");
```

Muestra cómo designar sustitutos de fuentes durante la carga.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = new FontSettings();

// Establezca una regla de sustitución de fuente para un objeto LoadOptions.
// Si el documento que estamos cargando utiliza una fuente que no tenemos,
// esta regla sustituirá la fuente no disponible por una que sí exista.
// En este caso, todos los usos de "MissingFont" se convertirán a "Comic Sans MS".
TableSubstitutionRule substitutionRule = loadOptions.FontSettings.SubstitutionSettings.TableSubstitution;
substitutionRule.AddSubstitutes("MissingFont", "Comic Sans MS");

Document doc = new Document(MyDir + "Missing font.html", loadOptions);

// En este punto, dicho texto todavía estará en "MissingFont".
//La sustitución de fuentes se realizará cuando rendericemos el documento.
Assert.AreEqual("MissingFont", doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Name);

doc.Save(ArtifactsDir + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```

### Ver también

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
