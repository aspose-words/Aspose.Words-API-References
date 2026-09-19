---
title: "Aspose::Words::Border::GetHashCode method"
linktitle: "GetHashCode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Border::GetHashCode method. Funziona come funzione hash per questo tipo in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words/border/gethashcode/
---
## Border::GetHashCode method


Funziona come funzione hash per questo tipo.

```cpp
int32_t Aspose::Words::Border::GetHashCode() const override
```


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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
