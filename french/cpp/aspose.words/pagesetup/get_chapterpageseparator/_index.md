---
title: "Méthode Aspose::Words::PageSetup::get_ChapterPageSeparator"
linktitle: "get_ChapterPageSeparator"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::PageSetup::get_ChapterPageSeparator. Obtient ou définit le caractère séparateur qui apparaît entre le numéro de chapitre et le numéro de page en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words/pagesetup/get_chapterpageseparator/
---
## PageSetup::get_ChapterPageSeparator method


Obtient ou définit le caractère séparateur qui apparaît entre le numéro du chapitre et le numéro de page.

```cpp
Aspose::Words::ChapterPageSeparator Aspose::Words::PageSetup::get_ChapterPageSeparator()
```

## Remarques


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

* Enum [ChapterPageSeparator](../../chapterpageseparator/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
