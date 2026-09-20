---
title: "clase Aspose::Words::Fonts::TableSubstitutionRule"
linktitle: "TableSubstitutionRule"
second_title: "Referencia de API de Aspose.Words para C++"
description: "clase Aspose::Words::Fonts::TableSubstitutionRule. Regla de sustitución de fuentes de tabla. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 18000
url: /es/cpp/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class


Regla de sustitución de fuentes de tabla. Para obtener más información, visite el artículo de documentación [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class TableSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Métodos

| Método | Descripción |
| --- | --- |
| [AddSubstitutes](./addsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Agrega nombres de fuentes sustitutas para el nombre de fuente original dado. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Especifica si la regla está habilitada o no. |
| [GetSubstitutes](./getsubstitutes/)(const System::String\&) | Devuelve una matriz que contiene los nombres de fuentes sustitutas para el nombre de fuente original especificado. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Load](./load/)(const System::String\&) | Carga la configuración de sustitución de tabla desde un archivo XML. |
| [Load](./load/)(const System::SharedPtr\<System::IO::Stream\>\&) | Carga la configuración de sustitución de tabla desde el flujo XML. |
| [LoadAndroidSettings](./loadandroidsettings/)() | Carga la configuración de sustitución de tabla predefinida para la plataforma Android. |
| [LoadLinuxSettings](./loadlinuxsettings/)() | Carga la configuración de sustitución de tabla predefinida para la plataforma Linux. |
| [LoadWindowsSettings](./loadwindowssettings/)() | Carga la configuración de sustitución de tabla predefinida para la plataforma Windows. |
| [Save](./save/)(const System::String\&) | Guarda la configuración actual de sustitución de tabla en un archivo. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Guarda la configuración actual de sustitución de tabla en un flujo. |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | Establecedor para [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| [SetSubstitutes](./setsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Sobrescribe los nombres de fuentes sustitutas para el nombre de fuente original dado. |
| static [Type](./type/)() |  |

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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
