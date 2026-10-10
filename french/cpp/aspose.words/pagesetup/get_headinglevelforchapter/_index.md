---
title: "Aspose::Words::PageSetup::get_HeadingLevelForChapter méthode"
linktitle: "get_HeadingLevelForChapter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup::get_HeadingLevelForChapter méthode. Obtient ou définit le style de niveau de titre appliqué aux titres de chapitres dans le document en C++."
type: docs
weight: 20000
url: /fr/cpp/aspose.words/pagesetup/get_headinglevelforchapter/
---
## PageSetup::get_HeadingLevelForChapter method


Obtient ou définit le style de niveau de titre appliqué aux titres de chapitres dans le document.

```cpp
int32_t Aspose::Words::PageSetup::get_HeadingLevelForChapter()
```

## Remarques


Peut être un nombre de 0 à 9. 0 signifie aucun numéro de chapitre s'il est appliqué au numéro de page.

Avant de pouvoir créer des numéros de page incluant les numéros de chapitre, les titres du document doivent avoir un format de plan numéroté appliqué.

## Exemples



Montre comment travailler avec les chapitres de page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_FirstSection()->get_PageSetup();

pageSetup->set_PageNumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
pageSetup->set_ChapterPageSeparator(Aspose::Words::ChapterPageSeparator::Colon);
pageSetup->set_HeadingLevelForChapter(1);
```

## Voir aussi

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
