---
title: "Aspose::Words::ChapterPageSeparator enum"
linktitle: "ChapterPageSeparator"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ChapterPageSeparator enum. Définit le caractère séparateur qui apparaît entre le chapitre et le numéro de page en C++."
type: docs
weight: 84000
url: /fr/cpp/aspose.words/chapterpageseparator/
---
## ChapterPageSeparator enum


Définit le caractère séparateur qui apparaît entre le numéro de chapitre et le numéro de page.

```cpp
enum class ChapterPageSeparator
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Trait d'union | 0 | Deux-points. |
| Point | 1 | Un point. |
| Deux-points | 2 | Deux-points. |
| Tiret cadratin | 3 | Un tiret emphatique. |
| Tiret demi-cadratin | 4 | Un tiret standard. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
