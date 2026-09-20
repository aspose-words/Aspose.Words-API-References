---
title: "Método Aspose::Words::Loading::LoadOptions::get_FontSettings"
linktitle: "get_FontSettings"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Loading::LoadOptions::get_FontSettings. Permite especificar la configuración de fuentes del documento en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.loading/loadoptions/get_fontsettings/
---
## LoadOptions::get_FontSettings method


Permite especificar la configuración de fuentes del documento.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Loading::LoadOptions::get_FontSettings() const
```

## Observaciones


Al cargar algunos formatos, Aspose.Words puede requerir resolver las fuentes. Por ejemplo, al cargar documentos HTML [Aspose.Words](../../../aspose.words/) puede resolver las fuentes para realizar una sustitución de fuentes.

Si se establece en **null**, se usarán la configuración estática de fuentes predeterminada [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/).

El valor predeterminado es **null**.

## Ejemplos



Muestra cómo designar sustitutos de fuentes durante la carga.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// Establece una regla de sustitución de fuentes para un objeto LoadOptions.
// Si el documento que estamos cargando usa una fuente que no tenemos,
// esta regla sustituirá la fuente no disponible por una que sí exista.
// En este caso, todos los usos de "MissingFont" se convertirán en "Comic Sans MS".
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> substitutionRule = loadOptions->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution();
substitutionRule->AddSubstitutes(u"MissingFont", System::MakeArray<System::String>({u"Comic Sans MS"}));

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.html", loadOptions);

// En este punto, dicho texto seguirá estando en "MissingFont".
// La sustitución de fuentes se realizará cuando rendericemos el documento.
ASSERT_EQ(u"MissingFont", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());

doc->Save(get_ArtifactsDir() + u"FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```


Muestra cómo aplicar la configuración de sustitución de fuentes al cargar un documento.
```cpp
// Crea un objeto FontSettings que sustituirá la fuente "Times New Roman"
// con la fuente "Arvo" de nuestra carpeta "MyFonts".
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->SetFontsFolder(get_FontsDir(), false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));

// Establece ese objeto FontSettings como una propiedad de un objeto LoadOptions recién creado.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(fontSettings);

// Carga el documento y luego renderízalo como PDF con la sustitución de fuentes.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.FontSettings.pdf");
```

## Ver también

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
