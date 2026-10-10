---
title: "Aspose::Words::ImportFormatOptions::get_ForceCopyStyles méthode"
linktitle: "get_ForceCopyStyles"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ImportFormatOptions::get_ForceCopyStyles méthode. Obtient ou définit une valeur booléenne indiquant s'il faut copier les styles conflictuels en mode KeepSourceFormatting. La valeur par défaut est false en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/importformatoptions/get_forcecopystyles/
---
## ImportFormatOptions::get_ForceCopyStyles method


Obtient ou définit une valeur booléenne indiquant s'il faut copier les styles conflictuels en mode [KeepSourceFormatting](../../importformatmode/). La valeur par défaut est **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ForceCopyStyles() const
```

## Remarques


Par défaut, si un style correspondant existe déjà dans un document de destination, le formatage du style source est développé en attributs de nœud directs et le style de ce nœud est réinitialisé à la valeur par défaut.

Lorsque cette option est définie sur **true**, le style source sera copié de force dans le document de destination avec un nom unique et appliqué au nœud importé.

Remarque, dans ce cas il n'est pas garanti que le formatage du nœud importé dans le document de destination soit préservé.

## Exemples



Montre comment copier les styles source avec des noms uniques de force.
```cpp
// Les deux documents contiennent MyStyle1 et MyStyle2, MyStyle3 n'existe que dans le document source.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ForceCopyStyles(true);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

System::SharedPtr<Aspose::Words::ParagraphCollection> paras = dstDoc->get_Sections()->idx_get(1)->get_Body()->get_Paragraphs();

ASSERT_EQ(paras->idx_get(0)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle1_0");
ASSERT_EQ(paras->idx_get(1)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle2_0");
ASSERT_EQ(paras->idx_get(2)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle3");
```

## Voir aussi

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
