---
title: "Aspose::Words::Vba::VbaProject clase"
linktitle: "VbaProject"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Vba::VbaProject. Proporciona acceso a la información del proyecto VBA. Un proyecto VBA dentro del documento se define como una colección de módulos VBA. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.vba/vbaproject/
---
## VbaProject class


Proporciona acceso a la información del proyecto VBA. Un proyecto VBA dentro del documento se define como una colección de módulos VBA. Para obtener más información, visite el artículo de documentación [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/).

```cpp
class VbaProject : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Clone](./clone/)() | Realiza una copia del [VbaProject](./). |
| [get_CodePage](./get_codepage/)() const | Obtiene o establece la página de códigos del proyecto VBA. |
| [get_IsProtected](./get_isprotected/)() | Muestra si el [VbaProject](./) está protegido con contraseña. |
| [get_IsSigned](./get_issigned/)() | Muestra si el [VbaProject](./) está firmado o no. |
| [get_Modules](./get_modules/)() | Devuelve la colección de módulos del proyecto VBA. |
| [get_Name](./get_name/)() const | Obtiene o establece el nombre del proyecto VBA. |
| [get_References](./get_references/)() | Obtiene una colección de referencias del proyecto VBA. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CodePage](./set_codepage/)(int32_t) | Método set para [Aspose::Words::Vba::VbaProject::get_CodePage](./get_codepage/). |
| [set_Name](./set_name/)(const System::String\&) | Método set para [Aspose::Words::Vba::VbaProject::get_Name](./get_name/). |
| static [Type](./type/)() |  |
| [VbaProject](./vbaproject/)() | Crea un [VbaProject](./) en blanco. |

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
