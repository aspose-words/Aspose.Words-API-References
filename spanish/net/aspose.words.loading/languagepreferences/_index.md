---
title: LanguagePreferences Class
linktitle: LanguagePreferences
articleTitle: LanguagePreferences
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.LanguagePreferences para personalizar y administrar sin esfuerzo la configuración de idioma para un mejor procesamiento de documentos.
type: docs
weight: 4100
url: /es/net/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class

Permite configurar las preferencias de idioma.

Para obtener más información, visite el[Especificar opciones de carga](https://docs.aspose.com/words/net/specify-load-options/) Artículo de documentación.

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
| [AddEditingLanguage](../../aspose.words.loading/languagepreferences/addeditinglanguage/)(*[EditingLanguage](../editinglanguage/)*) | Agrega lenguaje de edición adicional. |
| [AddEditingLanguages](../../aspose.words.loading/languagepreferences/addeditinglanguages/)(*EditingLanguage[]*) | Agrega idiomas de edición adicionales. |

## Observaciones

Implementa el cuadro de diálogo 'Establecer las preferencias de idioma de Office' en Word.

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

* espacio de nombres [Aspose.Words.Loading](../../aspose.words.loading/)
* asamblea [Aspose.Words](../../)
