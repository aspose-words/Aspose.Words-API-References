---
title: LanguagePreferences.DefaultEditingLanguage
linktitle: DefaultEditingLanguage
articleTitle: DefaultEditingLanguage
second_title: Aspose.Words para .NET
description: Gestiona tu experiencia de edición con la propiedad LanguagePreferences DefaultEditingLanguage. Configura y personaliza fácilmente tu idioma de edición predeterminado.
type: docs
weight: 20
url: /es/net/aspose.words.loading/languagepreferences/defaulteditinglanguage/
---
## LanguagePreferences.DefaultEditingLanguage property

Obtiene o establece el idioma de edición predeterminado.

El valor predeterminado esEnglishUS.

```csharp
public EditingLanguage DefaultEditingLanguage { get; set; }
```

## Ejemplos

Muestra cómo establecer un idioma predeterminado al cargar un documento.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.DefaultEditingLanguage = EditingLanguage.Russian;

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeId = doc.Styles.DefaultFont.LocaleId;
Console.WriteLine(localeId == (int)EditingLanguage.Russian
    ? "The document either has no any language set in defaults or it was set to Russian originally."
    : "The document default language was set to another than Russian language originally, so it is not overridden.");
```

### Ver también

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
