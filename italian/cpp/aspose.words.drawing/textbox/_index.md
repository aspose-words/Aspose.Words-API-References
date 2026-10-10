---
title: "Aspose::Words::Drawing::TextBox class"
linktitle: "CasellaDiTesto"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::TextBox class. Definisce gli attributi che specificano come un testo viene visualizzato all'interno di una forma. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words.drawing/textbox/
---
## TextBox class


Definisce gli attributi che specificano come un testo viene visualizzato all'interno di una forma. Per saperne di più, visita l'articolo di documentazione [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/).

```cpp
class TextBox : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [BreakForwardLink](./breakforwardlink/)() | Interrompe il collegamento al successivo [TextBox](./). |
| [get_FitShapeToText](./get_fitshapetotext/)() | Determina se Microsoft Word allargherà la forma per adattare il testo. |
| [get_InternalMarginBottom](./get_internalmarginbottom/)() | Specifica il margine interno inferiore in punti per una forma. |
| [get_InternalMarginLeft](./get_internalmarginleft/)() | Specifica il margine interno sinistro in punti per una forma. |
| [get_InternalMarginRight](./get_internalmarginright/)() | Specifica il margine interno destro in punti per una forma. |
| [get_InternalMarginTop](./get_internalmargintop/)() | Specifica il margine interno superiore in punti per una forma. |
| [get_LayoutFlow](./get_layoutflow/)() | Determina il flusso del layout del testo in una forma. |
| [get_Next](./get_next/)() | Restituisce o imposta un [TextBox](./) che rappresenta il successivo [TextBox](./) in una sequenza di forme. |
| [get_NoTextRotation](./get_notextrotation/)() | Ottiene o imposta un valore booleano che indica se il testo del [TextBox](./) non deve ruotare quando la forma è ruotata. |
| [get_Parent](./get_parent/)() const | Ottiene una forma genitore per il [TextBox](./). |
| [get_Previous](./get_previous/)() | Restituisce un [TextBox](./) che rappresenta il precedente [TextBox](./) in una sequenza di forme. |
| [get_TextBoxWrapMode](./get_textboxwrapmode/)() | Determina come il testo avvolge all'interno di una forma. |
| [get_VerticalAnchor](./get_verticalanchor/)() | Specifica l'allineamento verticale del testo all'interno di una forma. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsValidLinkTarget](./isvalidlinktarget/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | Determina se questo [TextBox](./) può essere collegato al [TextBox](./) di destinazione. |
| [set_FitShapeToText](./set_fitshapetotext/)(bool) | Impostatore per [Aspose::Words::Drawing::TextBox::get_FitShapeToText](./get_fitshapetotext/). |
| [set_InternalMarginBottom](./set_internalmarginbottom/)(double) | Impostatore per [Aspose::Words::Drawing::TextBox::get_InternalMarginBottom](./get_internalmarginbottom/). |
| [set_InternalMarginLeft](./set_internalmarginleft/)(double) | Impostatore per [Aspose::Words::Drawing::TextBox::get_InternalMarginLeft](./get_internalmarginleft/). |
| [set_InternalMarginRight](./set_internalmarginright/)(double) | Impostatore per [Aspose::Words::Drawing::TextBox::get_InternalMarginRight](./get_internalmarginright/). |
| [set_InternalMarginTop](./set_internalmargintop/)(double) | Impostatore per [Aspose::Words::Drawing::TextBox::get_InternalMarginTop](./get_internalmargintop/). |
| [set_LayoutFlow](./set_layoutflow/)(Aspose::Words::Drawing::LayoutFlow) | Impostatore per [Aspose::Words::Drawing::TextBox::get_LayoutFlow](./get_layoutflow/). |
| [set_Next](./set_next/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | Impostatore per [Aspose::Words::Drawing::TextBox::get_Next](./get_next/). |
| [set_NoTextRotation](./set_notextrotation/)(bool) | Impostatore per [Aspose::Words::Drawing::TextBox::get_NoTextRotation](./get_notextrotation/). |
| [set_TextBoxWrapMode](./set_textboxwrapmode/)(Aspose::Words::Drawing::TextBoxWrapMode) | Impostatore per [Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode](./get_textboxwrapmode/). |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::TextBoxAnchor) | Impostatore per [Aspose::Words::Drawing::TextBox::get_VerticalAnchor](./get_verticalanchor/). |
| static [Type](./type/)() |  |
## Note


Utilizza la proprietà [TextBox](../shape/get_textbox/) per accedere alle proprietà di testo di una forma. Non crei istanze della classe [TextBox](./) direttamente.

## Esempi



Mostra come impostare l'orientamento del testo all'interno di una casella di testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Sposta il costruttore del documento all'interno della TextBox e aggiungi del testo.
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// Imposta la proprietà "LayoutFlow" per definire un orientamento per il contenuto testuale di questa casella di testo.
textBox->set_LayoutFlow(layoutFlow);

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxLayoutFlow.docx");
```


Mostra come far ridimensionare una casella di testo affinché si adatti strettamente al suo contenuto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Applica questi valori a entrambi i membri per far sì che la forma padre si adatti
// strettamente attorno al contenuto del testo, ignorando le dimensioni impostate.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(Aspose::Words::Drawing::TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxFitShapeToText.docx");
```


Mostra come impostare i margini interni per una casella di testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un'altra casella di testo con margini specifici.
System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();
textBox->set_InternalMarginTop(15);
textBox->set_InternalMarginBottom(15);
textBox->set_InternalMarginLeft(15);
textBox->set_InternalMarginRight(15);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text placed according to textbox margins.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxMargins.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
