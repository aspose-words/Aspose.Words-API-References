---
title: "Aspose::Words::Drawing::ShapeBase::get_HRef méthode"
linktitle: "get_HRef"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_HRef méthode. Obtient ou définit l'adresse complète du lien hypertexte pour une forme en C++."
type: docs
weight: 24000
url: /fr/cpp/aspose.words.drawing/shapebase/get_href/
---
## ShapeBase::get_HRef method


Obtient ou définit l'adresse complète du lien hypertexte pour une forme.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_HRef()
```

## Remarques


La valeur par défaut est une chaîne vide.

Ci-dessous, des exemples de valeurs valides pour cette propriété :

URI complet: **https://www.aspose.com/**.

Nom complet du fichier: **C:\\My Documents\\SalesReport.doc**.

URI relatif: **%../../../resource.txt**

Nom de fichier relatif: **%..\\My Documents\\SalesReport.doc**.

[Bookmark](../../../aspose.words/bookmark/) within another document: **https://www.aspose.com/Products/Default.aspx::Suites**

[Bookmark](../../../aspose.words/bookmark/) within this document: **%#BookmakName**.

## Exemples



Montre comment insérer une forme contenant une image et qui est également un hyperlien.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_HRef(u"https://forum.aspose.com/");
shape->set_Target(u"New Window");
shape->set_ScreenTip(u"Aspose.Words Support Forums");

// Ctrl + clic gauche sur la forme dans Microsoft Word ouvrira une nouvelle fenêtre de navigateur web
// et nous amènera à l'hyperlien dans la propriété \"HRef\".
doc->Save(get_ArtifactsDir() + u"Image.InsertImageWithHyperlink.docx");
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
