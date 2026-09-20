---
title: "Método SetSubstitutes de Aspose::Words::Fonts::TableSubstitutionRule"
linktitle: "SetSubstitutes"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método SetSubstitutes de Aspose::Words::Fonts::TableSubstitutionRule. Sobrescribe los nombres de fuentes sustitutas para una fuente original dada en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule::SetSubstitutes method


Sobrescribe los nombres de fuentes sustitutas para el nombre de fuente original dado.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::SetSubstitutes(const System::String &originalFontName, const System::ArrayPtr<System::String> &substituteFontNames)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| originalFontName | const System::String\& | Nombre de fuente original. |
| substituteFontNames | const System::ArrayPtr\<System::String\>\& | Lista de nombres de fuentes alternativas. |

## Ejemplos



Muestra cómo establecer reglas de sustitución de fuentes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Hello world!");
builder->get_Font()->set_Name(u"Amethysta");
builder->Writeln(u"The quick brown fox jumps over the lazy dog.");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>> fontSources = Aspose::Words::Fonts::FontSettings::get_DefaultInstance()->GetFontsSources();

// Las fuentes predeterminadas contienen la primera fuente que usa el documento.
ASSERT_EQ(1, fontSources->get_Length());
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arial";
}))));

// La segunda fuente, "Amethysta", no está disponible.
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Amethysta";
}))));

// Podemos configurar una tabla de sustitución de fuentes que determina
// qué fuentes usará Aspose.Words como sustitutas de fuentes no disponibles.
// Establezca dos fuentes de sustitución para "Amethysta": "Arvo" y "Courier New".
// Si la primera sustituta no está disponible, Aspose.Words intentará usar la segunda sustituta, y así sucesivamente.
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->SetSubstitutes(u"Amethysta", System::MakeArray<System::String>({u"Arvo", u"Courier New"}));

// "Amethysta" no está disponible, y la regla de sustitución indica que la primera fuente a usar como sustituta es "Arvo".
ASSERT_FALSE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Arvo";
}))));

// "Arvo" tampoco está disponible, pero "Courier New" sí lo está.
ASSERT_TRUE(fontSources[0]->GetAvailableFonts()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f)>>([](System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo> f) -> bool
{
    return f->get_FullFontName() == u"Courier New";
}))));

// El documento de salida mostrará el texto que usa la fuente "Amethysta" formateada con "Courier New".
doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitution.pdf");
```


Muestra cómo trabajar con tablas de sustitución de fuentes personalizadas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Cree una nueva regla de sustitución de tabla y cargue la tabla de sustitución de fuentes predeterminada de Windows.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();

// Si seleccionamos fuentes exclusivamente de nuestra carpeta, necesitaremos una tabla de sustitución personalizada.
// Ya no tendremos acceso a las fuentes de Microsoft Windows,
// como "Arial" o "Times New Roman" ya que no existen en nuestra nueva carpeta de fuentes.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// A continuación se presentan dos formas de cargar una tabla de sustitución desde un archivo en el sistema de archivos local.
// 1 -  Desde un flujo:
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font substitution rules.xml", System::IO::FileMode::Open);
    tableSubstitutionRule->Load(fileStream);
}

// 2 -  Directamente desde un archivo:
tableSubstitutionRule->Load(get_MyDir() + u"Font substitution rules.xml");

// Dado que ya no tenemos acceso a "Arial", nuestra tabla de fuentes intentará primero sustituirla con "Nonexistent Font".
// No disponemos de esta fuente, por lo que pasará al siguiente sustituto, "Kreon", encontrado en la carpeta "MyFonts".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Missing Font", u"Kreon"}), tableSubstitutionRule->GetSubstitutes(u"Arial")->LINQ_ToArray());

// Podemos ampliar esta tabla programáticamente. Añadiremos una entrada que sustituya "Times New Roman" por "Arvo"
ASSERT_TRUE(System::TestTools::IsNull(tableSubstitutionRule->GetSubstitutes(u"Times New Roman")));
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Podemos agregar un sustituto de respaldo secundario para una entrada de fuente existente con AddSubstitutes().
// En caso de que "Arvo" no esté disponible, nuestra tabla buscará "M+ 2m" como segunda opción de sustituto.
tableSubstitutionRule->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Arvo", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// SetSubstitutes() puede establecer una nueva lista de fuentes sustitutas para una fuente.
tableSubstitutionRule->SetSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}));
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Squarish Sans CT", u"M+ 2m"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman")->LINQ_ToArray());

// Escribir texto con fuentes a las que no tenemos acceso activará nuestras reglas de sustitución.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Arial");
builder->Writeln(u"Text written in Arial, to be substituted by Kreon.");

builder->get_Font()->set_Name(u"Times New Roman");
builder->Writeln(u"Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Custom.pdf");
```

## Ver también

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
