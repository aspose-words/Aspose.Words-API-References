---
title: "Aspose::Words::Drawing::Fill::get_ForeTintAndShade méthode"
linktitle: "get_ForeTintAndShade"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::Fill::get_ForeTintAndShade méthode. Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur de premier plan en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.drawing/fill/get_foretintandshade/
---
## Fill::get_ForeTintAndShade method


Obtient ou définit une valeur double qui éclaircit ou assombrit la couleur de premier plan.

```cpp
double Aspose::Words::Drawing::Fill::get_ForeTintAndShade()
```

## Remarques


Les valeurs autorisées sont dans la plage de -1 (le plus sombre) à 1 (le plus clair) pour cette propriété.

Zéro (0) est neutre.

## Exemples



Montre comment gérer l'éclaircissement et l'assombrissement de la couleur de police du premier plan.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::SharedPtr<Aspose::Words::Drawing::Fill> textFill = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Fill();
textFill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Accent1);
if (textFill->get_ForeTintAndShade() == 0)
{
    textFill->set_ForeTintAndShade(0.5);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillTintAndShade.docx");
```

## Voir aussi

* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
