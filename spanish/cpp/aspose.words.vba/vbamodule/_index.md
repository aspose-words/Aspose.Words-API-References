---
title: "Aspose::Words::Vba::VbaModule class"
linktitle: "VbaModule"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Vba::VbaModule class. Proporciona acceso al módulo del proyecto VBA. Para obtener más información, visita el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.vba/vbamodule/
---
## VbaModule class


Proporciona acceso al módulo del proyecto VBA. Para obtener más información, visite el artículo de documentación [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/).

```cpp
class VbaModule : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Clone](./clone/)() | Realiza una copia del [VbaModule](./). |
| [get_Name](./get_name/)() const | Obtiene o establece el nombre del módulo del proyecto VBA. |
| [get_SourceCode](./get_sourcecode/)() const | Obtiene o establece el código fuente del módulo del proyecto VBA. |
| [get_Type](./get_type/)() const | Especifica si el módulo es un módulo procedural, módulo de documento, módulo de clase o módulo de diseñador. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Name](./set_name/)(const System::String\&) | Establecedor para [Aspose::Words::Vba::VbaModule::get_Name](./get_name/). |
| [set_SourceCode](./set_sourcecode/)(const System::String\&) | Establecedor para [Aspose::Words::Vba::VbaModule::get_SourceCode](./get_sourcecode/). |
| [set_Type](./set_type/)(Aspose::Words::Vba::VbaModuleType) | Establecedor para [Aspose::Words::Vba::VbaModule::get_Type](./get_type/). |
| static [Type](./type/)() |  |
| [VbaModule](./vbamodule/)() | Crea un módulo vacío. |

## Ejemplos



Muestra cómo acceder a la información del proyecto VBA de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");

// Un proyecto VBA contiene una colección de módulos VBA.
System::SharedPtr<Aspose::Words::Vba::VbaProject> vbaProject = doc->get_VbaProject();
std::cout << (vbaProject->get_IsSigned() ? System::String::Format(u"Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count()) : System::String::Format(u"Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count())) << std::endl;

System::SharedPtr<Aspose::Words::Vba::VbaModuleCollection> vbaModules = doc->get_VbaProject()->get_Modules();

ASSERT_EQ(vbaModules->LINQ_Count(), 3);

for (auto&& module_ : vbaModules)
{
    std::cout << System::String::Format(u"Module name: {0};\nModule code:\n{1}\n", module_->get_Name(), module_->get_SourceCode()) << std::endl;
}

// Establezca nuevo código fuente para el módulo VBA. Puede acceder a los módulos VBA en la colección ya sea por índice o por nombre.
vbaModules->idx_get(0)->set_SourceCode(u"Your VBA code...");
vbaModules->idx_get(u"Module1")->set_SourceCode(u"Your VBA code...");

// Elimine un módulo de la colección.
vbaModules->Remove(vbaModules->idx_get(2));
```

## Ver también

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
