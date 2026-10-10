---
title: "Aspose::Words::Document::get_VbaProject metodo"
linktitle: "get_VbaProject"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Document::get_VbaProject metodo. Ottiene o imposta un VbaProject in C++."
type: docs
weight: 56000
url: /it/cpp/aspose.words/document/get_vbaproject/
---
## Document::get_VbaProject method


Ottiene o imposta un [VbaProject](./).

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaProject> Aspose::Words::Document::get_VbaProject() const
```


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

* Class [VbaProject](../../../aspose.words.vba/vbaproject/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
