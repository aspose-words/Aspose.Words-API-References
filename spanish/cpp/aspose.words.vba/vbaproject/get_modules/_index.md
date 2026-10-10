---
title: "Método Aspose::Words::Vba::VbaProject::get_Modules"
linktitle: "get_Modules"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Vba::VbaProject::get_Modules. Devuelve la colección de módulos del proyecto VBA en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.vba/vbaproject/get_modules/
---
## VbaProject::get_Modules method


Devuelve la colección de módulos del proyecto VBA.

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaModuleCollection> Aspose::Words::Vba::VbaProject::get_Modules()
```


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

* Class [VbaModuleCollection](../../vbamodulecollection/)
* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
