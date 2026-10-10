---
title: "Metodo Aspose::Words::DocumentBuilder::InsertForms2OleControl"
linktitle: "InsertForms2OleControl"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::InsertForms2OleControl. Inserisce un oggetto Forms2OleControl nella posizione corrente in C++."
type: docs
weight: 35250
url: /it/cpp/aspose.words/documentbuilder/insertforms2olecontrol/
---
## DocumentBuilder::InsertForms2OleControl method


Inserisce l'oggetto [Forms2OleControl](../) nella posizione corrente.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertForms2OleControl(const System::SharedPtr<Aspose::Words::Drawing::Ole::Forms2OleControl> &forms2OleControl)
```


### ReturnValue

[Shape](../../../aspose.words.drawing/shape/) object that contains passed [Forms2OleControl](../)

## Esempi



Mostra come inserire un controllo ActiveX.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

auto button1 = System::MakeObject<Aspose::Words::Drawing::Ole::CommandButtonControl>();
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertForms2OleControl(button1);
ASSERT_EQ(Aspose::Words::Drawing::Ole::Forms2OleControlType::CommandButton, button1->get_Type());
```

## Vedi anche

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
