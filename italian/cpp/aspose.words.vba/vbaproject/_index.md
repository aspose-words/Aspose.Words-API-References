---
title: "Aspose::Words::Vba::VbaProject classe"
linktitle: "VbaProject"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Vba::VbaProject. Fornisce l'accesso alle informazioni del progetto VBA. Un progetto VBA all'interno del documento è definito come una raccolta di moduli VBA. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.vba/vbaproject/
---
## VbaProject class


Fornisce l'accesso alle informazioni del progetto VBA. Un progetto VBA all'interno del documento è definito come una raccolta di moduli VBA. Per saperne di più, visita l'articolo di documentazione [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/).

```cpp
class VbaProject : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Clone](./clone/)() | Esegue una copia del [VbaProject](./). |
| [get_CodePage](./get_codepage/)() const | Ottiene o imposta la pagina di codice del progetto VBA. |
| [get_IsProtected](./get_isprotected/)() | Indica se il [VbaProject](./) è protetto da password. |
| [get_IsSigned](./get_issigned/)() | Indica se il [VbaProject](./) è firmato o meno. |
| [get_Modules](./get_modules/)() | Restituisce la raccolta dei moduli del progetto VBA. |
| [get_Name](./get_name/)() const | Ottiene o imposta il nome del progetto VBA. |
| [get_References](./get_references/)() | Ottiene una raccolta di riferimenti del progetto VBA. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CodePage](./set_codepage/)(int32_t) | Impostatore per [Aspose::Words::Vba::VbaProject::get_CodePage](./get_codepage/). |
| [set_Name](./set_name/)(const System::String\&) | Impostatore per [Aspose::Words::Vba::VbaProject::get_Name](./get_name/). |
| static [Type](./type/)() |  |
| [VbaProject](./vbaproject/)() | Crea un [VbaProject](./) vuoto. |

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
