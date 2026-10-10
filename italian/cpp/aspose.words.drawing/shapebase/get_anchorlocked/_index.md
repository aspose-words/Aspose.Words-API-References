---
title: "Metodo get_AnchorLocked di Aspose::Words::Drawing::ShapeBase"
linktitle: "get_AnchorLocked"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo get_AnchorLocked di Aspose::Words::Drawing::ShapeBase. Specifica se l'ancora della forma è bloccata in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.drawing/shapebase/get_anchorlocked/
---
## ShapeBase::get_AnchorLocked method


Specifica se l'ancora della forma è bloccata.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AnchorLocked()
```

## Note


Il valore predefinito è **false**.

Ha effetto solo per le forme di livello superiore.

Questa proprietà influisce sul comportamento dell'ancora della forma in Microsoft Word. Quando l'ancora non è bloccata, spostare la forma in Microsoft Word può spostare anche l'ancora della forma.

## Esempi



Mostra come bloccare o sbloccare l'ancora del paragrafo di una forma.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

builder->Write(u"Our shape will have an anchor attached to this paragraph.");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 200, 160);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

builder->Writeln(u"Hello again!");

// Imposta la proprietà "AnchorLocked" su "true" per impedire l'ancora della forma
// di spostarsi quando si sposta la forma in Microsoft Word.
// Imposta la proprietà "AnchorLocked" su "false" per consentire qualsiasi movimento della forma
// per spostare anche la sua ancora verso qualsiasi altro paragrafo vicino a cui la forma si avvicina.
shape->set_AnchorLocked(anchorLocked);

// Se la forma non ha un simbolo di ancoraggio visibile a sinistra,
// dovremo abilitare gli ancoraggi visibili tramite "Opzioni" -> "Visualizza" -> "Ancoraggi oggetto".
doc->Save(get_ArtifactsDir() + u"Shape.AnchorLocked.docx");
```

## Vedi anche

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
