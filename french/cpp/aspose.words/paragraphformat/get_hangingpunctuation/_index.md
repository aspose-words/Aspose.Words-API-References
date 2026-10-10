---
title: "Aspose::Words::ParagraphFormat::get_HangingPunctuation méthode"
linktitle: "get_HangingPunctuation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphFormat::get_HangingPunctuation méthode. Obtient ou définit un indicateur indiquant si la ponctuation en retrait est activée pour le paragraphe actuel en C++."
type: docs
weight: 14000
url: /fr/cpp/aspose.words/paragraphformat/get_hangingpunctuation/
---
## ParagraphFormat::get_HangingPunctuation method


Obtient ou définit un indicateur indiquant si la ponctuation suspendue est activée pour le paragraphe actuel.

```cpp
bool Aspose::Words::ParagraphFormat::get_HangingPunctuation()
```


## Exemples



Montre comment définir des propriétés spéciales pour la typographie asiatique.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_FarEastLineBreakControl(true);
format->set_WordWrap(false);
format->set_HangingPunctuation(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.AsianTypographyProperties.docx");
```

## Voir aussi

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
