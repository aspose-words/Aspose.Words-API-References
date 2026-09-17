---
title: "Aspose::Words::Loading::BlockImportMode enum"
linktitle: "BlockImportMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::BlockImportMode enum. Spécifie comment les propriétés des éléments de niveau bloc sont importées depuis des documents basés sur HTML en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.loading/blockimportmode/
---
## BlockImportMode enum


Spécifie comment les propriétés des éléments de niveau bloc sont importées à partir de documents basés sur HTML.

```cpp
enum class BlockImportMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Merge | 0 | Les [Properties](../../aspose.words.properties/) des blocs parents sont fusionnées et stockées sur les éléments enfants (c.-à-d. paragraphes ou tableaux). |
| Preserve | 1 | Les [Properties](../../aspose.words.properties/) des blocs parents sont importées dans une structure logique spéciale et sont stockées séparément des nœuds du document. |


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

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
