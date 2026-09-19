---
title: "Aspose::Words::BorderCollection::idx_get metodo"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BorderCollection::idx_get metodo. Recupera un oggetto Border per tipo di bordo in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words/bordercollection/idx_get/
---
## BorderCollection::idx_get(Aspose::Words::BorderType) method


Recupera un oggetto [Border](../../border/) per tipo di bordo.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::idx_get(Aspose::Words::BorderType borderType)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| borderType | Aspose::Words::BorderType | Un valore [BorderType](../../bordertype/) che specifica il tipo di bordo da recuperare. |
## Note


Nota che non tutti i bordi sono presenti per i diversi elementi del documento. Questo metodo genera un'eccezione se richiedi un bordo non applicabile all'oggetto corrente.

## Esempi



Mostra come decorare il testo con bordi e ombreggiatura.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(Aspose::Words::BorderType::Left)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Right)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Top)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Bottom)->set_LineStyle(Aspose::Words::LineStyle::Double);

System::SharedPtr<Aspose::Words::Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.ApplyBordersAndShading.docx");
```

## Vedi anche

* Class [Border](../../border/)
* Enum [BorderType](../../bordertype/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## BorderCollection::idx_get(int32_t) method


Recupera un oggetto [Border](../../border/) per indice.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::idx_get(int32_t index)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | Indice basato su zero del bordo da recuperare. |

## Esempi



Mostra come le collezioni di bordi possono condividere elementi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Write(u"Paragraph 2.");

// Poiché abbiamo usato la stessa configurazione del bordo durante la creazione
// questi paragrafi, le loro collezioni di bordi condividono gli stessi elementi.
System::SharedPtr<Aspose::Words::BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
System::SharedPtr<Aspose::Words::BorderCollection> secondParagraphBorders = builder->get_CurrentParagraph()->get_ParagraphFormat()->get_Borders();

for (int32_t i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_TRUE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_EQ(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));
    ASSERT_FALSE(firstParagraphBorders->idx_get(i)->get_IsVisible());
}

for (auto&& border : System::IterateOver(secondParagraphBorders))
{
    border->set_LineStyle(Aspose::Words::LineStyle::DotDash);
}

// Dopo aver modificato lo stile della linea dei bordi solo nel secondo paragrafo,
// le collezioni di bordi non condividono più gli stessi elementi.
for (int32_t i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_FALSE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_NE(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));

    // Modificare l'aspetto di un bordo vuoto lo rende visibile.
    ASSERT_TRUE(secondParagraphBorders->idx_get(i)->get_IsVisible());
}

doc->Save(get_ArtifactsDir() + u"Border.SharedElements.docx");
```

## Vedi anche

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
