---
title: "Méthode Aspose::Words::DocumentBuilder::InsertForms2OleControl"
linktitle: "InsertForms2OleControl"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::InsertForms2OleControl. Insère un objet Forms2OleControl à la position actuelle en C++."
type: docs
weight: 35250
url: /fr/cpp/aspose.words/documentbuilder/insertforms2olecontrol/
---
## DocumentBuilder::InsertForms2OleControl method


Insère l'objet [Forms2OleControl](../) à la position actuelle.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertForms2OleControl(const System::SharedPtr<Aspose::Words::Drawing::Ole::Forms2OleControl> &forms2OleControl)
```


### ReturnValue

[Shape](../../../aspose.words.drawing/shape/) object that contains passed [Forms2OleControl](../)

## Exemples



Montre comment insérer un contrôle ActiveX.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

auto button1 = System::MakeObject<Aspose::Words::Drawing::Ole::CommandButtonControl>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertForms2OleControl(button1);
ASSERT_EQ(Aspose::Words::Drawing::Ole::Forms2OleControlType::CommandButton, button1->get_Type());
```

## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
