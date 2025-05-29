---
title: LanguagePreferences.AddEditingLanguage
linktitle: AddEditingLanguage
articleTitle: AddEditingLanguage
second_title: Aspose.Words para .NET
description: Mejore su experiencia de edición con el método AddEditingLanguage de LanguagePreferences. Añada y administre fácilmente varios idiomas de edición para un flujo de trabajo fluido.
type: docs
weight: 30
url: /es/net/aspose.words.loading/languagepreferences/addeditinglanguage/
---
## LanguagePreferences.AddEditingLanguage method

Agrega lenguaje de edición adicional.

```csharp
public void AddEditingLanguage(EditingLanguage language)
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

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
