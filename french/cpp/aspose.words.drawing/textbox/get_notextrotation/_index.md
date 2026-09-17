---
title: "Aspose::Words::Drawing::TextBox::get_NoTextRotation méthode"
linktitle: "get_NoTextRotation"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::TextBox::get_NoTextRotation méthode. Obtient ou définit une valeur booléenne indiquant que le texte du TextBox ne doit pas pivoter lorsque la forme est tournée en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.drawing/textbox/get_notextrotation/
---
## TextBox::get_NoTextRotation method


Obtient ou définit une valeur booléenne indiquant que le texte du [TextBox](../) ne doit pas pivoter lorsque la forme est tournée.

```cpp
bool Aspose::Words::Drawing::TextBox::get_NoTextRotation()
```

## Remarques


La valeur par défaut est **false**

## Exemples



Montre comment désactiver la rotation du texte lorsque la forme est tournée.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 20, 20);
shape->get_TextBox()->set_NoTextRotation(true);

doc->Save(get_ArtifactsDir() + u"Shape.NoTextRotation.docx");
```

## Voir aussi

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
