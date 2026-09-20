---
title: "Método Aspose::Words::Fonts::TableSubstitutionRule::Save"
linktitle: "Save"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fonts::TableSubstitutionRule::Save. Guarda la configuración actual de sustitución de tabla en un flujo en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.fonts/tablesubstitutionrule/save/
---
## TableSubstitutionRule::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Guarda la configuración actual de sustitución de tabla en un flujo.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::Save(const System::SharedPtr<System::IO::Stream> &outputStream)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Flujo de salida. |

## Ejemplos



Muestra cómo acceder a las tablas de sustitución de fuentes para Windows y Linux.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Crea una nueva regla de sustitución de tabla y carga la tabla de sustitución de fuentes predeterminada de Microsoft Windows.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();
tableSubstitutionRule->LoadWindowsSettings();

// En Windows, el sustituto predeterminado para la fuente "Times New Roman CE" es "Times New Roman".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Times New Roman"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Podemos guardar la tabla en forma de documento XML.
tableSubstitutionRule->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Windows.xml");

// Linux tiene su propia tabla de sustitución.
// Hay varias fuentes sustitutas para "Times New Roman CE".
// Si el primer sustituto, "FreeSerif", también está indisponible,
// esta regla recorrerá los demás en la matriz hasta encontrar uno disponible.
tableSubstitutionRule->LoadLinuxSettings();
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"FreeSerif", u"Liberation Serif", u"DejaVu Serif"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Guarda la tabla de sustitución de Linux en forma de documento XML usando un flujo.
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Linux.xml", System::IO::FileMode::Create);
    tableSubstitutionRule->Save(fileStream);
}
```

## Ver también

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## TableSubstitutionRule::Save(const System::String\&) method


Guarda la configuración actual de sustitución de tabla en un archivo.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::Save(const System::String &fileName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | Nombre del archivo de salida. |

## Ejemplos



Muestra cómo acceder a las tablas de sustitución de fuentes para Windows y Linux.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// Crea una nueva regla de sustitución de tabla y carga la tabla de sustitución de fuentes predeterminada de Microsoft Windows.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();
tableSubstitutionRule->LoadWindowsSettings();

// En Windows, el sustituto predeterminado para la fuente "Times New Roman CE" es "Times New Roman".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Times New Roman"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Podemos guardar la tabla en forma de documento XML.
tableSubstitutionRule->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Windows.xml");

// Linux tiene su propia tabla de sustitución.
// Hay varias fuentes sustitutas para "Times New Roman CE".
// Si el primer sustituto, "FreeSerif", también está indisponible,
// esta regla recorrerá los demás en la matriz hasta encontrar uno disponible.
tableSubstitutionRule->LoadLinuxSettings();
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"FreeSerif", u"Liberation Serif", u"DejaVu Serif"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// Guarda la tabla de sustitución de Linux en forma de documento XML usando un flujo.
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Linux.xml", System::IO::FileMode::Create);
    tableSubstitutionRule->Save(fileStream);
}
```

## Ver también

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
