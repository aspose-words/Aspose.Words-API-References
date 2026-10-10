---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode méthode"
linktitle: "get_BlockImportMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode méthode. Obtient ou définit une valeur qui spécifie comment les propriétés des éléments de niveau bloc sont importées. La valeur par défaut est Merge en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.loading/htmlloadoptions/get_blockimportmode/
---
## HtmlLoadOptions::get_BlockImportMode method


Obtient ou définit une valeur qui spécifie comment les propriétés des éléments de niveau bloc sont importées. La valeur par défaut est [Merge](../../blockimportmode/).

```cpp
Aspose::Words::Loading::BlockImportMode Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode() const
```


## Exemples



Montre comment les propriétés des éléments de niveau bloc sont importées depuis des documents basés sur HTML.
```cpp
const System::String html = u"\r\n            <html>\r\n                <div style='border:dotted'>\r\n                    <div style='border:solid'>\r\n                        <p>paragraph 1</p>\r\n                        <p>paragraph 2</p>\r\n                    </div>\r\n                </div>\r\n            </html>";
auto stream = System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html));

auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
// Définissez le nouveau mode d'importation des éléments de niveau bloc HTML.
loadOptions->set_BlockImportMode(blockImportMode);

auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BlockImport.docx");
```

## Voir aussi

* Enum [BlockImportMode](../../blockimportmode/)
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
