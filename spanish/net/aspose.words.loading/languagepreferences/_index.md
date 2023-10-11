---
title: Class LanguagePreferences
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Loading.LanguagePreferences clase. Permite configurar preferencias de idioma.
type: docs
weight: 3650
url: /es/net/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class

Permite configurar preferencias de idioma.

Para obtener más información, visite el[Especificar opciones de carga](https://docs.aspose.com/words/net/specify-load-options/) artículo de documentación.

```csharp
public class LanguagePreferences
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [LanguagePreferences](languagepreferences/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DefaultEditingLanguage](../../aspose.words.loading/languagepreferences/defaulteditinglanguage/) { get; set; } | Obtiene o establece el idioma de edición predeterminado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [AddEditingLanguage](../../aspose.words.loading/languagepreferences/addeditinglanguage/)(EditingLanguage) | Agrega idioma de edición adicional. |
| [AddEditingLanguages](../../aspose.words.loading/languagepreferences/addeditinglanguages/)(EditingLanguage[]) | Agrega idiomas de edición adicionales. |

### Observaciones

Implementa el cuadro de diálogo 'Establecer las preferencias de idioma de Office' en Word.

### Ejemplos

Muestra cómo aplicar preferencias de idioma al cargar un documento.

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

* espacio de nombres [Aspose.Words.Loading](../../aspose.words.loading/)
* asamblea [Aspose.Words](../../)


