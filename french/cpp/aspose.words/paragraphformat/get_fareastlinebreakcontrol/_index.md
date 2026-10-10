---
title: "Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl méthode"
linktitle: "get_FarEastLineBreakControl"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl méthode. Obtient ou définit un indicateur indiquant si les règles de césure asiatiques sont appliquées au paragraphe actuel en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words/paragraphformat/get_fareastlinebreakcontrol/
---
## ParagraphFormat::get_FarEastLineBreakControl method


Obtient ou définit un indicateur indiquant si les règles de césure est-asiatiques sont appliquées au paragraphe actuel.

```cpp
bool Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl()
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
