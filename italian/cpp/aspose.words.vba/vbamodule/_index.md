---
title: "Aspose::Words::Vba::VbaModule class"
linktitle: "VbaModule"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Vba::VbaModule class. Fornisce l'accesso al modulo del progetto VBA. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.vba/vbamodule/
---
## VbaModule class


Fornisce l'accesso al modulo del progetto VBA. Per saperne di più, visita l'articolo di documentazione [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/).

```cpp
class VbaModule : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Clone](./clone/)() | Esegue una copia di [VbaModule](./). |
| [get_Name](./get_name/)() const | Ottiene o imposta il nome del modulo del progetto VBA. |
| [get_SourceCode](./get_sourcecode/)() const | Ottiene o imposta il codice sorgente del modulo del progetto VBA. |
| [get_Type](./get_type/)() const | Specifica se il modulo è un modulo procedurale, modulo documento, modulo classe o modulo designer. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Name](./set_name/)(const System::String\&) | Impostatore per [Aspose::Words::Vba::VbaModule::get_Name](./get_name/). |
| [set_SourceCode](./set_sourcecode/)(const System::String\&) | Impostatore per [Aspose::Words::Vba::VbaModule::get_SourceCode](./get_sourcecode/). |
| [set_Type](./set_type/)(Aspose::Words::Vba::VbaModuleType) | Impostatore per [Aspose::Words::Vba::VbaModule::get_Type](./get_type/). |
| static [Type](./type/)() |  |
| [VbaModule](./vbamodule/)() | Crea un modulo vuoto. |

## Esempi



Mostra come accedere alle informazioni del progetto VBA di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");

// Un progetto VBA contiene una raccolta di moduli VBA.
System::SharedPtr<Aspose::Words::Vba::VbaProject> vbaProject = doc->get_VbaProject();
std::cout << (vbaProject->get_IsSigned() ? System::String::Format(u"Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count()) : System::String::Format(u"Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count())) << std::endl;

System::SharedPtr<Aspose::Words::Vba::VbaModuleCollection> vbaModules = doc->get_VbaProject()->get_Modules();

ASSERT_EQ(vbaModules->LINQ_Count(), 3);

for (auto&& module_ : vbaModules)
{
    std::cout << System::String::Format(u"Module name: {0};\nModule code:\n{1}\n", module_->get_Name(), module_->get_SourceCode()) << std::endl;
}

// Imposta nuovo codice sorgente per il modulo VBA. Puoi accedere ai moduli VBA nella collezione sia per indice che per nome.
vbaModules->idx_get(0)->set_SourceCode(u"Your VBA code...");
vbaModules->idx_get(u"Module1")->set_SourceCode(u"Your VBA code...");

// Rimuovi un modulo dalla collezione.
vbaModules->Remove(vbaModules->idx_get(2));
```

## Vedi anche

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
