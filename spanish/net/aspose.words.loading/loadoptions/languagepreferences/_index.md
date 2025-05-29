---
title: LoadOptions.LanguagePreferences
linktitle: LanguagePreferences
articleTitle: LanguagePreferences
second_title: Aspose.Words para .NET
description: Descubra LoadOptions LanguagePreferences para personalizar la carga de documentos con los idiomas preferidos, mejorando la experiencia del usuario y la accesibilidad.
type: docs
weight: 80
url: /es/net/aspose.words.loading/loadoptions/languagepreferences/
---
## LoadOptions.LanguagePreferences property

Obtiene las preferencias de idioma que se utilizarán cuando se cargue el documento.

```csharp
public LanguagePreferences LanguagePreferences { get; }
```

## Ejemplos

Muestra cómo aplicar las preferencias de idioma al cargar un documento.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.AddEditingLanguage(EditingLanguage.Japanese);

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeIdFarEast = doc.Styles.DefaultFont.LocaleIdFarEast;
Console.WriteLine(localeIdFarEast == (int)EditingLanguage.Japanese
    ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
    : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
```

### Ver también

* class [LanguagePreferences](../../languagepreferences/)
* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
